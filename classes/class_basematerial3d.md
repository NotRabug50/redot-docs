github\_url  
hide

# BaseMaterial3D

**Inherits:** `Material<class_Material>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:** `ORMMaterial3D<class_ORMMaterial3D>`,
`StandardMaterial3D<class_StandardMaterial3D>`

Abstract base class for defining the 3D rendering properties of meshes.

classref-introduction-group

## Description

This class serves as a default material with a wide variety of rendering
features and properties without the need to write shader code. See the
tutorial below for details.

classref-introduction-group

## Tutorials

-   `Standard Material 3D and ORM Material 3D <../tutorials/3d/standard_material_3d>`

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

## Enumerations

classref-enumeration

enum **TextureParam**: `🔗<enum_BaseMaterial3D_TextureParam>`

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_ALBEDO** =
`0`

Texture specifying per-pixel color.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_METALLIC** =
`1`

Texture specifying per-pixel metallic value.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_ROUGHNESS**
= `2`

Texture specifying per-pixel roughness value.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_EMISSION** =
`3`

Texture specifying per-pixel emission color.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_NORMAL** =
`4`

Texture specifying per-pixel normal vector.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_RIM** = `5`

Texture specifying per-pixel rim value.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_CLEARCOAT**
= `6`

Texture specifying per-pixel clearcoat value.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_FLOWMAP** =
`7`

Texture specifying per-pixel flowmap direction for use with
`anisotropy<class_BaseMaterial3D_property_anisotropy>`.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>`
**TEXTURE\_AMBIENT\_OCCLUSION** = `8`

Texture specifying per-pixel ambient occlusion value.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_HEIGHTMAP**
= `9`

Texture specifying per-pixel height.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>`
**TEXTURE\_SUBSURFACE\_SCATTERING** = `10`

Texture specifying per-pixel subsurface scattering.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>`
**TEXTURE\_SUBSURFACE\_TRANSMITTANCE** = `11`

Texture specifying per-pixel transmittance for subsurface scattering.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_BACKLIGHT**
= `12`

Texture specifying per-pixel backlight color.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_REFRACTION**
= `13`

Texture specifying per-pixel refraction strength.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>`
**TEXTURE\_DETAIL\_MASK** = `14`

Texture specifying per-pixel detail mask blending value.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>`
**TEXTURE\_DETAIL\_ALBEDO** = `15`

Texture specifying per-pixel detail color.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>`
**TEXTURE\_DETAIL\_NORMAL** = `16`

Texture specifying per-pixel detail normal.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_ORM** = `17`

Texture holding ambient occlusion, roughness, and metallic.

classref-enumeration-constant

`TextureParam<enum_BaseMaterial3D_TextureParam>` **TEXTURE\_MAX** = `18`

Represents the size of the
`TextureParam<enum_BaseMaterial3D_TextureParam>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureFilter**: `🔗<enum_BaseMaterial3D_TextureFilter>`

classref-enumeration-constant

`TextureFilter<enum_BaseMaterial3D_TextureFilter>`
**TEXTURE\_FILTER\_NEAREST** = `0`

The texture filter reads from the nearest pixel only. This makes the
texture look pixelated from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`TextureFilter<enum_BaseMaterial3D_TextureFilter>`
**TEXTURE\_FILTER\_LINEAR** = `1`

The texture filter blends between the nearest 4 pixels. This makes the
texture look smooth from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`TextureFilter<enum_BaseMaterial3D_TextureFilter>`
**TEXTURE\_FILTER\_NEAREST\_WITH\_MIPMAPS** = `2`

The texture filter reads from the nearest pixel and blends between the
nearest 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`). This makes the texture look pixelated from up close, and
smooth from a distance.

classref-enumeration-constant

`TextureFilter<enum_BaseMaterial3D_TextureFilter>`
**TEXTURE\_FILTER\_LINEAR\_WITH\_MIPMAPS** = `3`

The texture filter blends between the nearest 4 pixels and between the
nearest 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`). This makes the texture look smooth from up close, and smooth
from a distance.

classref-enumeration-constant

`TextureFilter<enum_BaseMaterial3D_TextureFilter>`
**TEXTURE\_FILTER\_NEAREST\_WITH\_MIPMAPS\_ANISOTROPIC** = `4`

The texture filter reads from the nearest pixel and blends between 2
mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`) based on the angle between the surface and the camera view.
This makes the texture look pixelated from up close, and smooth from a
distance. Anisotropic filtering improves texture quality on surfaces
that are almost in line with the camera, but is slightly slower. The
anisotropic filtering level can be changed by adjusting
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

classref-enumeration-constant

`TextureFilter<enum_BaseMaterial3D_TextureFilter>`
**TEXTURE\_FILTER\_LINEAR\_WITH\_MIPMAPS\_ANISOTROPIC** = `5`

The texture filter blends between the nearest 4 pixels and blends
between 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`) based on the angle between the surface and the camera view.
This makes the texture look smooth from up close, and smooth from a
distance. Anisotropic filtering improves texture quality on surfaces
that are almost in line with the camera, but is slightly slower. The
anisotropic filtering level can be changed by adjusting
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

classref-enumeration-constant

`TextureFilter<enum_BaseMaterial3D_TextureFilter>`
**TEXTURE\_FILTER\_MAX** = `6`

Represents the size of the
`TextureFilter<enum_BaseMaterial3D_TextureFilter>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DetailUV**: `🔗<enum_BaseMaterial3D_DetailUV>`

classref-enumeration-constant

`DetailUV<enum_BaseMaterial3D_DetailUV>` **DETAIL\_UV\_1** = `0`

Use `UV` with the detail texture.

classref-enumeration-constant

`DetailUV<enum_BaseMaterial3D_DetailUV>` **DETAIL\_UV\_2** = `1`

Use `UV2` with the detail texture.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Transparency**: `🔗<enum_BaseMaterial3D_Transparency>`

classref-enumeration-constant

`Transparency<enum_BaseMaterial3D_Transparency>`
**TRANSPARENCY\_DISABLED** = `0`

The material will not use transparency. This is the fastest to render.

classref-enumeration-constant

`Transparency<enum_BaseMaterial3D_Transparency>` **TRANSPARENCY\_ALPHA**
= `1`

The material will use the texture's alpha values for transparency. This
is the slowest to render, and disables shadow casting.

classref-enumeration-constant

`Transparency<enum_BaseMaterial3D_Transparency>`
**TRANSPARENCY\_ALPHA\_SCISSOR** = `2`

The material will cut off all values below a threshold, the rest will
remain opaque. The opaque portions will be rendered in the depth
prepass. This is faster to render than alpha blending, but slower than
opaque rendering. This also supports casting shadows.

classref-enumeration-constant

`Transparency<enum_BaseMaterial3D_Transparency>`
**TRANSPARENCY\_ALPHA\_HASH** = `3`

The material will cut off all values below a spatially-deterministic
threshold, the rest will remain opaque. This is faster to render than
alpha blending, but slower than opaque rendering. This also supports
casting shadows. Alpha hashing is suited for hair rendering.

classref-enumeration-constant

`Transparency<enum_BaseMaterial3D_Transparency>`
**TRANSPARENCY\_ALPHA\_DEPTH\_PRE\_PASS** = `4`

The material will use the texture's alpha value for transparency, but
will discard fragments with an alpha of less than 0.99 during the depth
prepass and fragments with an alpha less than 0.1 during the shadow
pass. This also supports casting shadows.

classref-enumeration-constant

`Transparency<enum_BaseMaterial3D_Transparency>` **TRANSPARENCY\_MAX** =
`5`

Represents the size of the
`Transparency<enum_BaseMaterial3D_Transparency>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ShadingMode**: `🔗<enum_BaseMaterial3D_ShadingMode>`

classref-enumeration-constant

`ShadingMode<enum_BaseMaterial3D_ShadingMode>`
**SHADING\_MODE\_UNSHADED** = `0`

The object will not receive shadows. This is the fastest to render, but
it disables all interactions with lights.

classref-enumeration-constant

`ShadingMode<enum_BaseMaterial3D_ShadingMode>`
**SHADING\_MODE\_PER\_PIXEL** = `1`

The object will be shaded per pixel. Useful for realistic shading
effects.

classref-enumeration-constant

`ShadingMode<enum_BaseMaterial3D_ShadingMode>`
**SHADING\_MODE\_PER\_VERTEX** = `2`

The object will be shaded per vertex. Useful when you want cheaper
shaders and do not care about visual quality. Not implemented yet (this
mode will act like
`SHADING_MODE_PER_PIXEL<class_BaseMaterial3D_constant_SHADING_MODE_PER_PIXEL>`).

classref-enumeration-constant

`ShadingMode<enum_BaseMaterial3D_ShadingMode>` **SHADING\_MODE\_MAX** =
`3`

Represents the size of the
`ShadingMode<enum_BaseMaterial3D_ShadingMode>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Feature**: `🔗<enum_BaseMaterial3D_Feature>`

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_EMISSION** = `0`

Constant for setting
`emission_enabled<class_BaseMaterial3D_property_emission_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_NORMAL\_MAPPING** =
`1`

Constant for setting
`normal_enabled<class_BaseMaterial3D_property_normal_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_RIM** = `2`

Constant for setting
`rim_enabled<class_BaseMaterial3D_property_rim_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_CLEARCOAT** = `3`

Constant for setting
`clearcoat_enabled<class_BaseMaterial3D_property_clearcoat_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_ANISOTROPY** = `4`

Constant for setting
`anisotropy_enabled<class_BaseMaterial3D_property_anisotropy_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_AMBIENT\_OCCLUSION** =
`5`

Constant for setting
`ao_enabled<class_BaseMaterial3D_property_ao_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_HEIGHT\_MAPPING** =
`6`

Constant for setting
`heightmap_enabled<class_BaseMaterial3D_property_heightmap_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>`
**FEATURE\_SUBSURFACE\_SCATTERING** = `7`

Constant for setting
`subsurf_scatter_enabled<class_BaseMaterial3D_property_subsurf_scatter_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>`
**FEATURE\_SUBSURFACE\_TRANSMITTANCE** = `8`

Constant for setting
`subsurf_scatter_transmittance_enabled<class_BaseMaterial3D_property_subsurf_scatter_transmittance_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_BACKLIGHT** = `9`

Constant for setting
`backlight_enabled<class_BaseMaterial3D_property_backlight_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_REFRACTION** = `10`

Constant for setting
`refraction_enabled<class_BaseMaterial3D_property_refraction_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_DETAIL** = `11`

Constant for setting
`detail_enabled<class_BaseMaterial3D_property_detail_enabled>`.

classref-enumeration-constant

`Feature<enum_BaseMaterial3D_Feature>` **FEATURE\_MAX** = `12`

Represents the size of the `Feature<enum_BaseMaterial3D_Feature>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BlendMode**: `🔗<enum_BaseMaterial3D_BlendMode>`

classref-enumeration-constant

`BlendMode<enum_BaseMaterial3D_BlendMode>` **BLEND\_MODE\_MIX** = `0`

Default blend mode. The color of the object is blended over the
background based on the object's alpha value.

classref-enumeration-constant

`BlendMode<enum_BaseMaterial3D_BlendMode>` **BLEND\_MODE\_ADD** = `1`

The color of the object is added to the background.

classref-enumeration-constant

`BlendMode<enum_BaseMaterial3D_BlendMode>` **BLEND\_MODE\_SUB** = `2`

The color of the object is subtracted from the background.

classref-enumeration-constant

`BlendMode<enum_BaseMaterial3D_BlendMode>` **BLEND\_MODE\_MUL** = `3`

The color of the object is multiplied by the background.

classref-enumeration-constant

`BlendMode<enum_BaseMaterial3D_BlendMode>`
**BLEND\_MODE\_PREMULT\_ALPHA** = `4`

The color of the object is added to the background and the alpha channel
is used to mask out the background. This is effectively a hybrid of the
blend mix and add modes, useful for effects like fire where you want the
flame to add but the smoke to mix. By default, this works with unshaded
materials using premultiplied textures. For shaded materials, use the
`PREMUL_ALPHA_FACTOR` built-in so that lighting can be modulated as
well.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AlphaAntiAliasing**: `🔗<enum_BaseMaterial3D_AlphaAntiAliasing>`

classref-enumeration-constant

`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
**ALPHA\_ANTIALIASING\_OFF** = `0`

Disables Alpha AntiAliasing for the material.

classref-enumeration-constant

`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
**ALPHA\_ANTIALIASING\_ALPHA\_TO\_COVERAGE** = `1`

Enables AlphaToCoverage. Alpha values in the material are passed to the
AntiAliasing sample mask.

classref-enumeration-constant

`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
**ALPHA\_ANTIALIASING\_ALPHA\_TO\_COVERAGE\_AND\_TO\_ONE** = `2`

Enables AlphaToCoverage and forces all non-zero alpha values to `1`.
Alpha values in the material are passed to the AntiAliasing sample mask.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DepthDrawMode**: `🔗<enum_BaseMaterial3D_DepthDrawMode>`

classref-enumeration-constant

`DepthDrawMode<enum_BaseMaterial3D_DepthDrawMode>`
**DEPTH\_DRAW\_OPAQUE\_ONLY** = `0`

Default depth draw mode. Depth is drawn only for opaque objects during
the opaque prepass (if any) and during the opaque pass.

classref-enumeration-constant

`DepthDrawMode<enum_BaseMaterial3D_DepthDrawMode>`
**DEPTH\_DRAW\_ALWAYS** = `1`

Objects will write to depth during the opaque and the transparent
passes. Transparent objects that are close to the camera may obscure
other transparent objects behind them.

\*\*Note:\*\* This does not influence whether transparent objects are
included in the depth prepass or not. For that, see
`Transparency<enum_BaseMaterial3D_Transparency>`.

classref-enumeration-constant

`DepthDrawMode<enum_BaseMaterial3D_DepthDrawMode>`
**DEPTH\_DRAW\_DISABLED** = `2`

Objects will not write their depth to the depth buffer, even during the
depth prepass (if enabled).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CullMode**: `🔗<enum_BaseMaterial3D_CullMode>`

classref-enumeration-constant

`CullMode<enum_BaseMaterial3D_CullMode>` **CULL\_BACK** = `0`

Default cull mode. The back of the object is culled when not visible.
Back face triangles will be culled when facing the camera. This results
in only the front side of triangles being drawn. For closed-surface
meshes, this means that only the exterior of the mesh will be visible.

classref-enumeration-constant

`CullMode<enum_BaseMaterial3D_CullMode>` **CULL\_FRONT** = `1`

Front face triangles will be culled when facing the camera. This results
in only the back side of triangles being drawn. For closed-surface
meshes, this means that the interior of the mesh will be drawn instead
of the exterior.

classref-enumeration-constant

`CullMode<enum_BaseMaterial3D_CullMode>` **CULL\_DISABLED** = `2`

No face culling is performed; both the front face and back face will be
visible.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Flags**: `🔗<enum_BaseMaterial3D_Flags>`

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_DISABLE\_DEPTH\_TEST** = `0`

Disables the depth test, so this object is drawn on top of all others
drawn before it. This puts the object in the transparent draw pass where
it is sorted based on distance to camera. Objects drawn after it in the
draw order may cover it. This also disables writing to depth.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_ALBEDO\_FROM\_VERTEX\_COLOR**
= `1`

Set `ALBEDO` to the per-vertex color specified in the mesh.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_SRGB\_VERTEX\_COLOR** = `2`

Vertex colors are considered to be stored in sRGB color space and are
converted to linear color space during rendering. See also
`vertex_color_is_srgb<class_BaseMaterial3D_property_vertex_color_is_srgb>`.

\*\*Note:\*\* Only effective when using the Forward+ and Mobile
rendering methods.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_USE\_POINT\_SIZE** = `3`

Uses point size to alter the size of primitive points. Also changes the
albedo texture lookup to use `POINT_COORD` instead of `UV`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_FIXED\_SIZE** = `4`

Object is scaled by depth so that it always appears the same size on
screen.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_BILLBOARD\_KEEP\_SCALE** =
`5`

Shader will keep the scale set for the mesh. Otherwise the scale is lost
when billboarding. Only applies when
`billboard_mode<class_BaseMaterial3D_property_billboard_mode>` is
`BILLBOARD_ENABLED<class_BaseMaterial3D_constant_BILLBOARD_ENABLED>`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_UV1\_USE\_TRIPLANAR** = `6`

Use triplanar texture lookup for all texture lookups that would normally
use `UV`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_UV2\_USE\_TRIPLANAR** = `7`

Use triplanar texture lookup for all texture lookups that would normally
use `UV2`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_UV1\_USE\_WORLD\_TRIPLANAR**
= `8`

Use triplanar texture lookup for all texture lookups that would normally
use `UV`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_UV2\_USE\_WORLD\_TRIPLANAR**
= `9`

Use triplanar texture lookup for all texture lookups that would normally
use `UV2`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_AO\_ON\_UV2** = `10`

Use `UV2` coordinates to look up from the
`ao_texture<class_BaseMaterial3D_property_ao_texture>`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_EMISSION\_ON\_UV2** = `11`

Use `UV2` coordinates to look up from the
`emission_texture<class_BaseMaterial3D_property_emission_texture>`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>`
**FLAG\_ALBEDO\_TEXTURE\_FORCE\_SRGB** = `12`

Forces the shader to convert albedo from sRGB space to linear space. See
also
`albedo_texture_force_srgb<class_BaseMaterial3D_property_albedo_texture_force_srgb>`.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_DONT\_RECEIVE\_SHADOWS** =
`13`

Disables receiving shadows from other objects.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_DISABLE\_AMBIENT\_LIGHT** =
`14`

Disables receiving ambient light.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_USE\_SHADOW\_TO\_OPACITY** =
`15`

Enables the shadow to opacity feature.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_USE\_TEXTURE\_REPEAT** = `16`

Enables the texture to repeat when UV coordinates are outside the 0-1
range. If using one of the linear filtering modes, this can result in
artifacts at the edges of a texture when the sampler filters across the
edges of the texture.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_INVERT\_HEIGHTMAP** = `17`

Invert values read from a depth texture to convert them to height values
(heightmap).

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_SUBSURFACE\_MODE\_SKIN** =
`18`

Enables the skin mode for subsurface scattering which is used to improve
the look of subsurface scattering when used for human skin.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_PARTICLE\_TRAILS\_MODE** =
`19`

Enables parts of the shader required for
`GPUParticles3D<class_GPUParticles3D>` trails to function. This also
requires using a mesh with appropriate skinning, such as
`RibbonTrailMesh<class_RibbonTrailMesh>` or
`TubeTrailMesh<class_TubeTrailMesh>`. Enabling this feature outside of
materials used in `GPUParticles3D<class_GPUParticles3D>` meshes will
break material rendering.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_ALBEDO\_TEXTURE\_MSDF** =
`20`

Enables multichannel signed distance field rendering shader.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_DISABLE\_FOG** = `21`

Disables receiving depth-based or volumetric fog.

classref-enumeration-constant

`Flags<enum_BaseMaterial3D_Flags>` **FLAG\_MAX** = `22`

Represents the size of the `Flags<enum_BaseMaterial3D_Flags>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DiffuseMode**: `🔗<enum_BaseMaterial3D_DiffuseMode>`

classref-enumeration-constant

`DiffuseMode<enum_BaseMaterial3D_DiffuseMode>` **DIFFUSE\_BURLEY** = `0`

Default diffuse scattering algorithm.

classref-enumeration-constant

`DiffuseMode<enum_BaseMaterial3D_DiffuseMode>` **DIFFUSE\_LAMBERT** =
`1`

Diffuse scattering ignores roughness.

classref-enumeration-constant

`DiffuseMode<enum_BaseMaterial3D_DiffuseMode>`
**DIFFUSE\_LAMBERT\_WRAP** = `2`

Extends Lambert to cover more than 90 degrees when roughness increases.

classref-enumeration-constant

`DiffuseMode<enum_BaseMaterial3D_DiffuseMode>` **DIFFUSE\_TOON** = `3`

Uses a hard cut for lighting, with smoothing affected by roughness.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SpecularMode**: `🔗<enum_BaseMaterial3D_SpecularMode>`

classref-enumeration-constant

`SpecularMode<enum_BaseMaterial3D_SpecularMode>`
**SPECULAR\_SCHLICK\_GGX** = `0`

Default specular blob.

classref-enumeration-constant

`SpecularMode<enum_BaseMaterial3D_SpecularMode>` **SPECULAR\_TOON** =
`1`

Toon blob which changes size based on roughness.

classref-enumeration-constant

`SpecularMode<enum_BaseMaterial3D_SpecularMode>` **SPECULAR\_DISABLED**
= `2`

No specular blob. This is slightly faster to render than other specular
modes.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BillboardMode**: `🔗<enum_BaseMaterial3D_BillboardMode>`

classref-enumeration-constant

`BillboardMode<enum_BaseMaterial3D_BillboardMode>`
**BILLBOARD\_DISABLED** = `0`

Billboard mode is disabled.

classref-enumeration-constant

`BillboardMode<enum_BaseMaterial3D_BillboardMode>`
**BILLBOARD\_ENABLED** = `1`

The object's Z axis will always face the camera.

classref-enumeration-constant

`BillboardMode<enum_BaseMaterial3D_BillboardMode>`
**BILLBOARD\_FIXED\_Y** = `2`

The object's X axis will always face the camera.

classref-enumeration-constant

`BillboardMode<enum_BaseMaterial3D_BillboardMode>`
**BILLBOARD\_PARTICLES** = `3`

Used for particle systems when assigned to
`GPUParticles3D<class_GPUParticles3D>` and
`CPUParticles3D<class_CPUParticles3D>` nodes (flipbook animation).
Enables `particles_anim_*` properties.

The
`ParticleProcessMaterial.anim_speed_min<class_ParticleProcessMaterial_property_anim_speed_min>`
or
`CPUParticles3D.anim_speed_min<class_CPUParticles3D_property_anim_speed_min>`
should also be set to a value bigger than zero for the animation to
play.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureChannel**: `🔗<enum_BaseMaterial3D_TextureChannel>`

classref-enumeration-constant

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**TEXTURE\_CHANNEL\_RED** = `0`

Used to read from the red channel of a texture.

classref-enumeration-constant

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**TEXTURE\_CHANNEL\_GREEN** = `1`

Used to read from the green channel of a texture.

classref-enumeration-constant

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**TEXTURE\_CHANNEL\_BLUE** = `2`

Used to read from the blue channel of a texture.

classref-enumeration-constant

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**TEXTURE\_CHANNEL\_ALPHA** = `3`

Used to read from the alpha channel of a texture.

classref-enumeration-constant

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**TEXTURE\_CHANNEL\_GRAYSCALE** = `4`

Used to read from the linear (non-perceptual) average of the red, green
and blue channels of a texture.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EmissionOperator**: `🔗<enum_BaseMaterial3D_EmissionOperator>`

classref-enumeration-constant

`EmissionOperator<enum_BaseMaterial3D_EmissionOperator>`
**EMISSION\_OP\_ADD** = `0`

Adds the emission color to the color from the emission texture.

classref-enumeration-constant

`EmissionOperator<enum_BaseMaterial3D_EmissionOperator>`
**EMISSION\_OP\_MULTIPLY** = `1`

Multiplies the emission color by the color from the emission texture.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DistanceFadeMode**: `🔗<enum_BaseMaterial3D_DistanceFadeMode>`

classref-enumeration-constant

`DistanceFadeMode<enum_BaseMaterial3D_DistanceFadeMode>`
**DISTANCE\_FADE\_DISABLED** = `0`

Do not use distance fade.

classref-enumeration-constant

`DistanceFadeMode<enum_BaseMaterial3D_DistanceFadeMode>`
**DISTANCE\_FADE\_PIXEL\_ALPHA** = `1`

Smoothly fades the object out based on each pixel's distance from the
camera using the alpha channel.

classref-enumeration-constant

`DistanceFadeMode<enum_BaseMaterial3D_DistanceFadeMode>`
**DISTANCE\_FADE\_PIXEL\_DITHER** = `2`

Smoothly fades the object out based on each pixel's distance from the
camera using a dithering approach. Dithering discards pixels based on a
set pattern to smoothly fade without enabling transparency. On certain
hardware, this can be faster than
`DISTANCE_FADE_PIXEL_ALPHA<class_BaseMaterial3D_constant_DISTANCE_FADE_PIXEL_ALPHA>`.

classref-enumeration-constant

`DistanceFadeMode<enum_BaseMaterial3D_DistanceFadeMode>`
**DISTANCE\_FADE\_OBJECT\_DITHER** = `3`

Smoothly fades the object out based on the object's distance from the
camera using a dithering approach. Dithering discards pixels based on a
set pattern to smoothly fade without enabling transparency. On certain
hardware, this can be faster than
`DISTANCE_FADE_PIXEL_ALPHA<class_BaseMaterial3D_constant_DISTANCE_FADE_PIXEL_ALPHA>`
and
`DISTANCE_FADE_PIXEL_DITHER<class_BaseMaterial3D_constant_DISTANCE_FADE_PIXEL_DITHER>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Color<class_Color>` **albedo\_color** = `Color(1, 1, 1, 1)`
`🔗<class_BaseMaterial3D_property_albedo_color>`

classref-property-setget

-   `void (No return value.)` **set\_albedo**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_albedo**()

The material's base color.

\*\*Note:\*\* If
`detail_enabled<class_BaseMaterial3D_property_detail_enabled>` is `true`
and a `detail_albedo<class_BaseMaterial3D_property_detail_albedo>`
texture is specified,
`albedo_color<class_BaseMaterial3D_property_albedo_color>` will *not*
modulate the detail texture. This can be used to color partial areas of
a material by not specifying an albedo texture and using a transparent
`detail_albedo<class_BaseMaterial3D_property_detail_albedo>` texture
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **albedo\_texture**
`🔗<class_BaseMaterial3D_property_albedo_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture to multiply by
`albedo_color<class_BaseMaterial3D_property_albedo_color>`. Used for
basic texturing of objects.

If the texture appears unexpectedly too dark or too bright, check
`albedo_texture_force_srgb<class_BaseMaterial3D_property_albedo_texture_force_srgb>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **albedo\_texture\_force\_srgb** = `false`
`🔗<class_BaseMaterial3D_property_albedo_texture_force_srgb>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, forces a conversion of the
`albedo_texture<class_BaseMaterial3D_property_albedo_texture>` from sRGB
color space to linear color space. See also
`vertex_color_is_srgb<class_BaseMaterial3D_property_vertex_color_is_srgb>`.

This should only be enabled when needed (typically when using a
`ViewportTexture<class_ViewportTexture>` as
`albedo_texture<class_BaseMaterial3D_property_albedo_texture>`). If
`albedo_texture_force_srgb<class_BaseMaterial3D_property_albedo_texture_force_srgb>`
is `true` when it shouldn't be, the texture will appear to be too dark.
If
`albedo_texture_force_srgb<class_BaseMaterial3D_property_albedo_texture_force_srgb>`
is `false` when it shouldn't be, the texture will appear to be too
bright.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **albedo\_texture\_msdf** = `false`
`🔗<class_BaseMaterial3D_property_albedo_texture_msdf>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Enables multichannel signed distance field rendering shader. Use
`msdf_pixel_range<class_BaseMaterial3D_property_msdf_pixel_range>` and
`msdf_outline_size<class_BaseMaterial3D_property_msdf_outline_size>` to
configure MSDF parameters.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **alpha\_antialiasing\_edge**
`🔗<class_BaseMaterial3D_property_alpha_antialiasing_edge>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_antialiasing\_edge**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_antialiasing\_edge**()

Threshold at which antialiasing will be applied on the alpha channel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
**alpha\_antialiasing\_mode**
`🔗<class_BaseMaterial3D_property_alpha_antialiasing_mode>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_antialiasing**(value:
    `AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`)
-   `AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
    **get\_alpha\_antialiasing**()

The type of alpha antialiasing to apply. See
`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **alpha\_hash\_scale**
`🔗<class_BaseMaterial3D_property_alpha_hash_scale>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_hash\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_hash\_scale**()

The hashing scale for Alpha Hash. Recommended values between `0` and
`2`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **alpha\_scissor\_threshold**
`🔗<class_BaseMaterial3D_property_alpha_scissor_threshold>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_scissor\_threshold**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_scissor\_threshold**()

Threshold at which the alpha scissor will discard values. Higher values
will result in more pixels being discarded. If the material becomes too
opaque at a distance, try increasing
`alpha_scissor_threshold<class_BaseMaterial3D_property_alpha_scissor_threshold>`.
If the material disappears at a distance, try decreasing
`alpha_scissor_threshold<class_BaseMaterial3D_property_alpha_scissor_threshold>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anisotropy** = `0.0`
`🔗<class_BaseMaterial3D_property_anisotropy>`

classref-property-setget

-   `void (No return value.)` **set\_anisotropy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_anisotropy**()

The strength of the anisotropy effect. This is multiplied by
`anisotropy_flowmap<class_BaseMaterial3D_property_anisotropy_flowmap>`'s
alpha channel if a texture is defined there and the texture contains an
alpha channel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **anisotropy\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_anisotropy_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, anisotropy is enabled. Anisotropy changes the shape of the
specular blob and aligns it to tangent space. This is useful for brushed
aluminium and hair reflections.

\*\*Note:\*\* Mesh tangents are needed for anisotropy to work. If the
mesh does not contain tangents, the anisotropy effect will appear
broken.

\*\*Note:\*\* Material anisotropy should not to be confused with
anisotropic texture filtering, which can be enabled by setting
`texture_filter<class_BaseMaterial3D_property_texture_filter>` to
`TEXTURE_FILTER_LINEAR_WITH_MIPMAPS_ANISOTROPIC<class_BaseMaterial3D_constant_TEXTURE_FILTER_LINEAR_WITH_MIPMAPS_ANISOTROPIC>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **anisotropy\_flowmap**
`🔗<class_BaseMaterial3D_property_anisotropy_flowmap>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture that offsets the tangent map for anisotropy calculations and
optionally controls the anisotropy effect (if an alpha channel is
present). The flowmap texture is expected to be a derivative map, with
the red channel representing distortion on the X axis and green channel
representing distortion on the Y axis. Values below 0.5 will result in
negative distortion, whereas values above 0.5 will result in positive
distortion.

If present, the texture's alpha channel will be used to multiply the
strength of the `anisotropy<class_BaseMaterial3D_property_anisotropy>`
effect. Fully opaque pixels will keep the anisotropy effect's original
strength while fully transparent pixels will disable the anisotropy
effect entirely. The flowmap texture's blue channel is ignored.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ao\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_ao_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, ambient occlusion is enabled. Ambient occlusion darkens areas
based on the `ao_texture<class_BaseMaterial3D_property_ao_texture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ao\_light\_affect** = `0.0`
`🔗<class_BaseMaterial3D_property_ao_light_affect>`

classref-property-setget

-   `void (No return value.)` **set\_ao\_light\_affect**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ao\_light\_affect**()

Amount that ambient occlusion affects lighting from lights. If `0`,
ambient occlusion only affects ambient light. If `1`, ambient occlusion
affects lights just as much as it affects ambient light. This can be
used to impact the strength of the ambient occlusion effect, but
typically looks unrealistic.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ao\_on\_uv2** = `false`
`🔗<class_BaseMaterial3D_property_ao_on_uv2>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, use `UV2` coordinates to look up from the
`ao_texture<class_BaseMaterial3D_property_ao_texture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **ao\_texture**
`🔗<class_BaseMaterial3D_property_ao_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture that defines the amount of ambient occlusion for a given point
on the object.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**ao\_texture\_channel** = `0`
`🔗<class_BaseMaterial3D_property_ao_texture_channel>`

classref-property-setget

-   `void (No return value.)` **set\_ao\_texture\_channel**(value:
    `TextureChannel<enum_BaseMaterial3D_TextureChannel>`)
-   `TextureChannel<enum_BaseMaterial3D_TextureChannel>`
    **get\_ao\_texture\_channel**()

Specifies the channel of the
`ao_texture<class_BaseMaterial3D_property_ao_texture>` in which the
ambient occlusion information is stored. This is useful when you store
the information for multiple effects in a single texture. For example if
you stored metallic in the red channel, roughness in the blue, and
ambient occlusion in the green you could reduce the number of textures
you use.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **backlight** = `Color(0, 0, 0, 1)`
`🔗<class_BaseMaterial3D_property_backlight>`

classref-property-setget

-   `void (No return value.)` **set\_backlight**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_backlight**()

The color used by the backlight effect. Represents the light passing
through an object.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **backlight\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_backlight_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the backlight effect is enabled. See also
`subsurf_scatter_transmittance_enabled<class_BaseMaterial3D_property_subsurf_scatter_transmittance_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **backlight\_texture**
`🔗<class_BaseMaterial3D_property_backlight_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture used to control the backlight effect per-pixel. Added to
`backlight<class_BaseMaterial3D_property_backlight>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **billboard\_keep\_scale** = `false`
`🔗<class_BaseMaterial3D_property_billboard_keep_scale>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the shader will keep the scale set for the mesh. Otherwise,
the scale is lost when billboarding. Only applies when
`billboard_mode<class_BaseMaterial3D_property_billboard_mode>` is not
`BILLBOARD_DISABLED<class_BaseMaterial3D_constant_BILLBOARD_DISABLED>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BillboardMode<enum_BaseMaterial3D_BillboardMode>` **billboard\_mode** =
`0` `🔗<class_BaseMaterial3D_property_billboard_mode>`

classref-property-setget

-   `void (No return value.)` **set\_billboard\_mode**(value:
    `BillboardMode<enum_BaseMaterial3D_BillboardMode>`)
-   `BillboardMode<enum_BaseMaterial3D_BillboardMode>`
    **get\_billboard\_mode**()

Controls how the object faces the camera. See
`BillboardMode<enum_BaseMaterial3D_BillboardMode>`.

\*\*Note:\*\* When billboarding is enabled and the material also casts
shadows, billboards will face **the** camera in the scene when rendering
shadows. In scenes with multiple cameras, the intended shadow cannot be
determined and this will result in undefined behavior. See [GitHub Pull
Request \#72638](https://github.com/godotengine/godot/pull/72638) for
details.

\*\*Note:\*\* Billboard mode is not suitable for VR because the
left-right vector of the camera is not horizontal when the screen is
attached to your head instead of on the table. See [GitHub issue
\#41567](https://github.com/godotengine/godot/issues/41567) for details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BlendMode<enum_BaseMaterial3D_BlendMode>` **blend\_mode** = `0`
`🔗<class_BaseMaterial3D_property_blend_mode>`

classref-property-setget

-   `void (No return value.)` **set\_blend\_mode**(value:
    `BlendMode<enum_BaseMaterial3D_BlendMode>`)
-   `BlendMode<enum_BaseMaterial3D_BlendMode>` **get\_blend\_mode**()

The material's blend mode.

\*\*Note:\*\* Values other than `Mix` force the object into the
transparent pipeline. See `BlendMode<enum_BaseMaterial3D_BlendMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **clearcoat** = `1.0`
`🔗<class_BaseMaterial3D_property_clearcoat>`

classref-property-setget

-   `void (No return value.)` **set\_clearcoat**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_clearcoat**()

Sets the strength of the clearcoat effect. Setting to `0` looks the same
as disabling the clearcoat effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **clearcoat\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_clearcoat_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, clearcoat rendering is enabled. Adds a secondary transparent
pass to the lighting calculation resulting in an added specular blob.
This makes materials appear as if they have a clear layer on them that
can be either glossy or rough.

\*\*Note:\*\* Clearcoat rendering is not visible if the material's
`shading_mode<class_BaseMaterial3D_property_shading_mode>` is
`SHADING_MODE_UNSHADED<class_BaseMaterial3D_constant_SHADING_MODE_UNSHADED>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **clearcoat\_roughness** = `0.5`
`🔗<class_BaseMaterial3D_property_clearcoat_roughness>`

classref-property-setget

-   `void (No return value.)` **set\_clearcoat\_roughness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_clearcoat\_roughness**()

Sets the roughness of the clearcoat pass. A higher value results in a
rougher clearcoat while a lower value results in a smoother clearcoat.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **clearcoat\_texture**
`🔗<class_BaseMaterial3D_property_clearcoat_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture that defines the strength of the clearcoat effect and the
glossiness of the clearcoat. Strength is specified in the red channel
while glossiness is specified in the green channel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CullMode<enum_BaseMaterial3D_CullMode>` **cull\_mode** = `0`
`🔗<class_BaseMaterial3D_property_cull_mode>`

classref-property-setget

-   `void (No return value.)` **set\_cull\_mode**(value:
    `CullMode<enum_BaseMaterial3D_CullMode>`)
-   `CullMode<enum_BaseMaterial3D_CullMode>` **get\_cull\_mode**()

Determines which side of the triangle to cull depending on whether the
triangle faces towards or away from the camera. See
`CullMode<enum_BaseMaterial3D_CullMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DepthDrawMode<enum_BaseMaterial3D_DepthDrawMode>` **depth\_draw\_mode**
= `0` `🔗<class_BaseMaterial3D_property_depth_draw_mode>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_draw\_mode**(value:
    `DepthDrawMode<enum_BaseMaterial3D_DepthDrawMode>`)
-   `DepthDrawMode<enum_BaseMaterial3D_DepthDrawMode>`
    **get\_depth\_draw\_mode**()

Determines when depth rendering takes place. See
`DepthDrawMode<enum_BaseMaterial3D_DepthDrawMode>`. See also
`transparency<class_BaseMaterial3D_property_transparency>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **detail\_albedo**
`🔗<class_BaseMaterial3D_property_detail_albedo>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture that specifies the color of the detail overlay.
`detail_albedo<class_BaseMaterial3D_property_detail_albedo>`'s alpha
channel is used as a mask, even when the material is opaque. To use a
dedicated texture as a mask, see
`detail_mask<class_BaseMaterial3D_property_detail_mask>`.

\*\*Note:\*\*
`detail_albedo<class_BaseMaterial3D_property_detail_albedo>` is *not*
modulated by `albedo_color<class_BaseMaterial3D_property_albedo_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BlendMode<enum_BaseMaterial3D_BlendMode>` **detail\_blend\_mode** = `0`
`🔗<class_BaseMaterial3D_property_detail_blend_mode>`

classref-property-setget

-   `void (No return value.)` **set\_detail\_blend\_mode**(value:
    `BlendMode<enum_BaseMaterial3D_BlendMode>`)
-   `BlendMode<enum_BaseMaterial3D_BlendMode>`
    **get\_detail\_blend\_mode**()

Specifies how the
`detail_albedo<class_BaseMaterial3D_property_detail_albedo>` should
blend with the current `ALBEDO`. See
`BlendMode<enum_BaseMaterial3D_BlendMode>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **detail\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_detail_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, enables the detail overlay. Detail is a second texture that
gets mixed over the surface of the object based on
`detail_mask<class_BaseMaterial3D_property_detail_mask>` and
`detail_albedo<class_BaseMaterial3D_property_detail_albedo>`'s alpha
channel. This can be used to add variation to objects, or to blend
between two different albedo/normal textures.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **detail\_mask**
`🔗<class_BaseMaterial3D_property_detail_mask>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture used to specify how the detail textures get blended with the
base textures. `detail_mask<class_BaseMaterial3D_property_detail_mask>`
can be used together with
`detail_albedo<class_BaseMaterial3D_property_detail_albedo>`'s alpha
channel (if any).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **detail\_normal**
`🔗<class_BaseMaterial3D_property_detail_normal>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture that specifies the per-pixel normal of the detail overlay. The
`detail_normal<class_BaseMaterial3D_property_detail_normal>` texture
only uses the red and green channels; the blue and alpha channels are
ignored. The normal read from
`detail_normal<class_BaseMaterial3D_property_detail_normal>` is oriented
around the surface normal provided by the `Mesh<class_Mesh>`.

\*\*Note:\*\* Godot expects the normal map to use X+, Y+, and Z+
coordinates. See [this
page](http://wiki.polycount.com/wiki/Normal_Map_Technical_Details#Common_Swizzle_Coordinates)
for a comparison of normal map coordinates expected by popular engines.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DetailUV<enum_BaseMaterial3D_DetailUV>` **detail\_uv\_layer** = `0`
`🔗<class_BaseMaterial3D_property_detail_uv_layer>`

classref-property-setget

-   `void (No return value.)` **set\_detail\_uv**(value:
    `DetailUV<enum_BaseMaterial3D_DetailUV>`)
-   `DetailUV<enum_BaseMaterial3D_DetailUV>` **get\_detail\_uv**()

Specifies whether to use `UV` or `UV2` for the detail layer. See
`DetailUV<enum_BaseMaterial3D_DetailUV>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DiffuseMode<enum_BaseMaterial3D_DiffuseMode>` **diffuse\_mode** = `0`
`🔗<class_BaseMaterial3D_property_diffuse_mode>`

classref-property-setget

-   `void (No return value.)` **set\_diffuse\_mode**(value:
    `DiffuseMode<enum_BaseMaterial3D_DiffuseMode>`)
-   `DiffuseMode<enum_BaseMaterial3D_DiffuseMode>`
    **get\_diffuse\_mode**()

The algorithm used for diffuse light scattering. See
`DiffuseMode<enum_BaseMaterial3D_DiffuseMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disable\_ambient\_light** = `false`
`🔗<class_BaseMaterial3D_property_disable_ambient_light>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the object receives no ambient light.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disable\_fog** = `false`
`🔗<class_BaseMaterial3D_property_disable_fog>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the object will not be affected by fog (neither volumetric
nor depth fog). This is useful for unshaded or transparent materials
(e.g. particles), which without this setting will be affected even if
fully transparent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disable\_receive\_shadows** = `false`
`🔗<class_BaseMaterial3D_property_disable_receive_shadows>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the object receives no shadow that would otherwise be cast
onto it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **distance\_fade\_max\_distance** = `10.0`
`🔗<class_BaseMaterial3D_property_distance_fade_max_distance>`

classref-property-setget

-   `void (No return value.)`
    **set\_distance\_fade\_max\_distance**(value: `float<class_float>`)
-   `float<class_float>` **get\_distance\_fade\_max\_distance**()

Distance at which the object appears fully opaque.

\*\*Note:\*\* If
`distance_fade_max_distance<class_BaseMaterial3D_property_distance_fade_max_distance>`
is less than
`distance_fade_min_distance<class_BaseMaterial3D_property_distance_fade_min_distance>`,
the behavior will be reversed. The object will start to fade away at
`distance_fade_max_distance<class_BaseMaterial3D_property_distance_fade_max_distance>`
and will fully disappear once it reaches
`distance_fade_min_distance<class_BaseMaterial3D_property_distance_fade_min_distance>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **distance\_fade\_min\_distance** = `0.0`
`🔗<class_BaseMaterial3D_property_distance_fade_min_distance>`

classref-property-setget

-   `void (No return value.)`
    **set\_distance\_fade\_min\_distance**(value: `float<class_float>`)
-   `float<class_float>` **get\_distance\_fade\_min\_distance**()

Distance at which the object starts to become visible. If the object is
less than this distance away, it will be invisible.

\*\*Note:\*\* If
`distance_fade_min_distance<class_BaseMaterial3D_property_distance_fade_min_distance>`
is greater than
`distance_fade_max_distance<class_BaseMaterial3D_property_distance_fade_max_distance>`,
the behavior will be reversed. The object will start to fade away at
`distance_fade_max_distance<class_BaseMaterial3D_property_distance_fade_max_distance>`
and will fully disappear once it reaches
`distance_fade_min_distance<class_BaseMaterial3D_property_distance_fade_min_distance>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DistanceFadeMode<enum_BaseMaterial3D_DistanceFadeMode>`
**distance\_fade\_mode** = `0`
`🔗<class_BaseMaterial3D_property_distance_fade_mode>`

classref-property-setget

-   `void (No return value.)` **set\_distance\_fade**(value:
    `DistanceFadeMode<enum_BaseMaterial3D_DistanceFadeMode>`)
-   `DistanceFadeMode<enum_BaseMaterial3D_DistanceFadeMode>`
    **get\_distance\_fade**()

Specifies which type of fade to use. Can be any of the
`DistanceFadeMode<enum_BaseMaterial3D_DistanceFadeMode>`s.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **emission** = `Color(0, 0, 0, 1)`
`🔗<class_BaseMaterial3D_property_emission>`

classref-property-setget

-   `void (No return value.)` **set\_emission**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_emission**()

The emitted light's color. See
`emission_enabled<class_BaseMaterial3D_property_emission_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **emission\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_emission_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the body emits light. Emitting light makes the object appear
brighter. The object can also cast light on other objects if a
`VoxelGI<class_VoxelGI>`, SDFGI, or `LightmapGI<class_LightmapGI>` is
used and this object is used in baked lighting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_energy\_multiplier** = `1.0`
`🔗<class_BaseMaterial3D_property_emission_energy_multiplier>`

classref-property-setget

-   `void (No return value.)`
    **set\_emission\_energy\_multiplier**(value: `float<class_float>`)
-   `float<class_float>` **get\_emission\_energy\_multiplier**()

Multiplier for emitted light. See
`emission_enabled<class_BaseMaterial3D_property_emission_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_intensity**
`🔗<class_BaseMaterial3D_property_emission_intensity>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_intensity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_emission\_intensity**()

Luminance of emitted light, measured in nits (candela per square meter).
Only available when
`ProjectSettings.rendering/lights_and_shadows/use_physical_light_units<class_ProjectSettings_property_rendering/lights_and_shadows/use_physical_light_units>`
is enabled. The default is roughly equivalent to an indoor lightbulb.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **emission\_on\_uv2** = `false`
`🔗<class_BaseMaterial3D_property_emission_on_uv2>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Use `UV2` to read from the
`emission_texture<class_BaseMaterial3D_property_emission_texture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`EmissionOperator<enum_BaseMaterial3D_EmissionOperator>`
**emission\_operator** = `0`
`🔗<class_BaseMaterial3D_property_emission_operator>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_operator**(value:
    `EmissionOperator<enum_BaseMaterial3D_EmissionOperator>`)
-   `EmissionOperator<enum_BaseMaterial3D_EmissionOperator>`
    **get\_emission\_operator**()

Sets how `emission<class_BaseMaterial3D_property_emission>` interacts
with `emission_texture<class_BaseMaterial3D_property_emission_texture>`.
Can either add or multiply. See
`EmissionOperator<enum_BaseMaterial3D_EmissionOperator>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **emission\_texture**
`🔗<class_BaseMaterial3D_property_emission_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture that specifies how much surface emits light at a given point.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **fixed\_size** = `false`
`🔗<class_BaseMaterial3D_property_fixed_size>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the object is rendered at the same size regardless of
distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **grow** = `false`
`🔗<class_BaseMaterial3D_property_grow>`

classref-property-setget

-   `void (No return value.)` **set\_grow\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_grow\_enabled**()

If `true`, enables the vertex grow setting. This can be used to create
mesh-based outlines using a second material pass and its
`cull_mode<class_BaseMaterial3D_property_cull_mode>` set to
`CULL_FRONT<class_BaseMaterial3D_constant_CULL_FRONT>`. See also
`grow_amount<class_BaseMaterial3D_property_grow_amount>`.

\*\*Note:\*\* Vertex growth cannot create new vertices, which means that
visible gaps may occur in sharp corners. This can be alleviated by
designing the mesh to use smooth normals exclusively using [face
weighted normals](https://wiki.polycount.com/wiki/Face_weighted_normals)
in the 3D authoring software. In this case, grow will be able to join
every outline together, just like in the original mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **grow\_amount** = `0.0`
`🔗<class_BaseMaterial3D_property_grow_amount>`

classref-property-setget

-   `void (No return value.)` **set\_grow**(value: `float<class_float>`)
-   `float<class_float>` **get\_grow**()

Grows object vertices in the direction of their normals. Only effective
if `grow<class_BaseMaterial3D_property_grow>` is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **heightmap\_deep\_parallax** = `false`
`🔗<class_BaseMaterial3D_property_heightmap_deep_parallax>`

classref-property-setget

-   `void (No return value.)` **set\_heightmap\_deep\_parallax**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_heightmap\_deep\_parallax\_enabled**()

If `true`, uses parallax occlusion mapping to represent depth in the
material instead of simple offset mapping (see
`heightmap_enabled<class_BaseMaterial3D_property_heightmap_enabled>`).
This results in a more convincing depth effect, but is much more
expensive on the GPU. Only enable this on materials where it makes a
significant visual difference.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **heightmap\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_heightmap_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, height mapping is enabled (also called "parallax mapping" or
"depth mapping"). See also
`normal_enabled<class_BaseMaterial3D_property_normal_enabled>`. Height
mapping is a demanding feature on the GPU, so it should only be used on
materials where it makes a significant visual difference.

\*\*Note:\*\* Height mapping is not supported if triplanar mapping is
used on the same material. The value of
`heightmap_enabled<class_BaseMaterial3D_property_heightmap_enabled>`
will be ignored if
`uv1_triplanar<class_BaseMaterial3D_property_uv1_triplanar>` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **heightmap\_flip\_binormal** = `false`
`🔗<class_BaseMaterial3D_property_heightmap_flip_binormal>`

classref-property-setget

-   `void (No return value.)`
    **set\_heightmap\_deep\_parallax\_flip\_binormal**(value:
    `bool<class_bool>`)
-   `bool<class_bool>`
    **get\_heightmap\_deep\_parallax\_flip\_binormal**()

If `true`, flips the mesh's binormal vectors when interpreting the
height map. If the heightmap effect looks strange when the camera moves
(even with a reasonable
`heightmap_scale<class_BaseMaterial3D_property_heightmap_scale>`), try
setting this to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **heightmap\_flip\_tangent** = `false`
`🔗<class_BaseMaterial3D_property_heightmap_flip_tangent>`

classref-property-setget

-   `void (No return value.)`
    **set\_heightmap\_deep\_parallax\_flip\_tangent**(value:
    `bool<class_bool>`)
-   `bool<class_bool>`
    **get\_heightmap\_deep\_parallax\_flip\_tangent**()

If `true`, flips the mesh's tangent vectors when interpreting the height
map. If the heightmap effect looks strange when the camera moves (even
with a reasonable
`heightmap_scale<class_BaseMaterial3D_property_heightmap_scale>`), try
setting this to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **heightmap\_flip\_texture** = `false`
`🔗<class_BaseMaterial3D_property_heightmap_flip_texture>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, interprets the height map texture as a depth map, with
brighter values appearing to be "lower" in altitude compared to darker
values.

This can be enabled for compatibility with some materials authored for
Godot 3.x. This is not necessary if the Invert import option was used to
invert the depth map in Godot 3.x, in which case
`heightmap_flip_texture<class_BaseMaterial3D_property_heightmap_flip_texture>`
should remain `false`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **heightmap\_max\_layers**
`🔗<class_BaseMaterial3D_property_heightmap_max_layers>`

classref-property-setget

-   `void (No return value.)`
    **set\_heightmap\_deep\_parallax\_max\_layers**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_heightmap\_deep\_parallax\_max\_layers**()

The number of layers to use for parallax occlusion mapping when the
camera is up close to the material. Higher values result in a more
convincing depth effect, especially in materials that have steep height
changes. Higher values have a significant cost on the GPU, so it should
only be increased on materials where it makes a significant visual
difference.

\*\*Note:\*\* Only effective if
`heightmap_deep_parallax<class_BaseMaterial3D_property_heightmap_deep_parallax>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **heightmap\_min\_layers**
`🔗<class_BaseMaterial3D_property_heightmap_min_layers>`

classref-property-setget

-   `void (No return value.)`
    **set\_heightmap\_deep\_parallax\_min\_layers**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_heightmap\_deep\_parallax\_min\_layers**()

The number of layers to use for parallax occlusion mapping when the
camera is far away from the material. Higher values result in a more
convincing depth effect, especially in materials that have steep height
changes. Higher values have a significant cost on the GPU, so it should
only be increased on materials where it makes a significant visual
difference.

\*\*Note:\*\* Only effective if
`heightmap_deep_parallax<class_BaseMaterial3D_property_heightmap_deep_parallax>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **heightmap\_scale** = `5.0`
`🔗<class_BaseMaterial3D_property_heightmap_scale>`

classref-property-setget

-   `void (No return value.)` **set\_heightmap\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_heightmap\_scale**()

The heightmap scale to use for the parallax effect (see
`heightmap_enabled<class_BaseMaterial3D_property_heightmap_enabled>`).
The default value is tuned so that the highest point (value = 255)
appears to be 5 cm higher than the lowest point (value = 0). Higher
values result in a deeper appearance, but may result in artifacts
appearing when looking at the material from oblique angles, especially
when the camera moves. Negative values can be used to invert the
parallax effect, but this is different from inverting the texture using
`heightmap_flip_texture<class_BaseMaterial3D_property_heightmap_flip_texture>`
as the material will also appear to be "closer" to the camera. In most
cases, `heightmap_scale<class_BaseMaterial3D_property_heightmap_scale>`
should be kept to a positive value.

\*\*Note:\*\* If the height map effect looks strange regardless of this
value, try adjusting
`heightmap_flip_binormal<class_BaseMaterial3D_property_heightmap_flip_binormal>`
and
`heightmap_flip_tangent<class_BaseMaterial3D_property_heightmap_flip_tangent>`.
See also
`heightmap_texture<class_BaseMaterial3D_property_heightmap_texture>` for
recommendations on authoring heightmap textures, as the way the
heightmap texture is authored affects how
`heightmap_scale<class_BaseMaterial3D_property_heightmap_scale>`
behaves.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **heightmap\_texture**
`🔗<class_BaseMaterial3D_property_heightmap_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The texture to use as a height map. See also
`heightmap_enabled<class_BaseMaterial3D_property_heightmap_enabled>`.

For best results, the texture should be normalized (with
`heightmap_scale<class_BaseMaterial3D_property_heightmap_scale>` reduced
to compensate). In [GIMP](https://gimp.org), this can be done using
**Colors &gt; Auto &gt; Equalize**. If the texture only uses a small
part of its available range, the parallax effect may look strange,
especially when the camera moves.

\*\*Note:\*\* To reduce memory usage and improve loading times, you may
be able to use a lower-resolution heightmap texture as most heightmaps
are only comprised of low-frequency data.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **metallic** = `0.0`
`🔗<class_BaseMaterial3D_property_metallic>`

classref-property-setget

-   `void (No return value.)` **set\_metallic**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_metallic**()

A high value makes the material appear more like a metal. Non-metals use
their albedo as the diffuse color and add diffuse to the specular
reflection. With non-metals, the reflection appears on top of the albedo
color. Metals use their albedo as a multiplier to the specular
reflection and set the diffuse color to black resulting in a tinted
reflection. Materials work better when fully metal or fully non-metal,
values between `0` and `1` should only be used for blending between
metal and non-metal sections. To alter the amount of reflection use
`roughness<class_BaseMaterial3D_property_roughness>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **metallic\_specular** = `0.5`
`🔗<class_BaseMaterial3D_property_metallic_specular>`

classref-property-setget

-   `void (No return value.)` **set\_specular**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_specular**()

Adjusts the strength of specular reflections. Specular reflections are
composed of scene reflections and the specular lobe which is the bright
spot that is reflected from light sources. When set to `0.0`, no
specular reflections will be visible. This differs from the
`SPECULAR_DISABLED<class_BaseMaterial3D_constant_SPECULAR_DISABLED>`
`SpecularMode<enum_BaseMaterial3D_SpecularMode>` as
`SPECULAR_DISABLED<class_BaseMaterial3D_constant_SPECULAR_DISABLED>`
only applies to the specular lobe from the light source.

\*\*Note:\*\* Unlike `metallic<class_BaseMaterial3D_property_metallic>`,
this is not energy-conserving, so it should be left at `0.5` in most
cases. See also `roughness<class_BaseMaterial3D_property_roughness>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **metallic\_texture**
`🔗<class_BaseMaterial3D_property_metallic_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture used to specify metallic for an object. This is multiplied by
`metallic<class_BaseMaterial3D_property_metallic>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**metallic\_texture\_channel** = `0`
`🔗<class_BaseMaterial3D_property_metallic_texture_channel>`

classref-property-setget

-   `void (No return value.)` **set\_metallic\_texture\_channel**(value:
    `TextureChannel<enum_BaseMaterial3D_TextureChannel>`)
-   `TextureChannel<enum_BaseMaterial3D_TextureChannel>`
    **get\_metallic\_texture\_channel**()

Specifies the channel of the
`metallic_texture<class_BaseMaterial3D_property_metallic_texture>` in
which the metallic information is stored. This is useful when you store
the information for multiple effects in a single texture. For example if
you stored metallic in the red channel, roughness in the blue, and
ambient occlusion in the green you could reduce the number of textures
you use.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **msdf\_outline\_size** = `0.0`
`🔗<class_BaseMaterial3D_property_msdf_outline_size>`

classref-property-setget

-   `void (No return value.)` **set\_msdf\_outline\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_msdf\_outline\_size**()

The width of the shape outline.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **msdf\_pixel\_range** = `4.0`
`🔗<class_BaseMaterial3D_property_msdf_pixel_range>`

classref-property-setget

-   `void (No return value.)` **set\_msdf\_pixel\_range**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_msdf\_pixel\_range**()

The width of the range around the shape between the minimum and maximum
representable signed distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **no\_depth\_test** = `false`
`🔗<class_BaseMaterial3D_property_no_depth_test>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, depth testing is disabled and the object will be drawn in
render order.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **normal\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_normal_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, normal mapping is enabled. This has a slight performance
cost, especially on mobile GPUs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **normal\_scale** = `1.0`
`🔗<class_BaseMaterial3D_property_normal_scale>`

classref-property-setget

-   `void (No return value.)` **set\_normal\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_normal\_scale**()

The strength of the normal map's effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **normal\_texture**
`🔗<class_BaseMaterial3D_property_normal_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture used to specify the normal at a given pixel. The
`normal_texture<class_BaseMaterial3D_property_normal_texture>` only uses
the red and green channels; the blue and alpha channels are ignored. The
normal read from
`normal_texture<class_BaseMaterial3D_property_normal_texture>` is
oriented around the surface normal provided by the `Mesh<class_Mesh>`.

\*\*Note:\*\* The mesh must have both normals and tangents defined in
its vertex data. Otherwise, the normal map won't render correctly and
will only appear to darken the whole surface. If creating geometry with
`SurfaceTool<class_SurfaceTool>`, you can use
`SurfaceTool.generate_normals<class_SurfaceTool_method_generate_normals>`
and
`SurfaceTool.generate_tangents<class_SurfaceTool_method_generate_tangents>`
to automatically generate normals and tangents respectively.

\*\*Note:\*\* Godot expects the normal map to use X+, Y+, and Z+
coordinates. See [this
page](http://wiki.polycount.com/wiki/Normal_Map_Technical_Details#Common_Swizzle_Coordinates)
for a comparison of normal map coordinates expected by popular engines.

\*\*Note:\*\* If
`detail_enabled<class_BaseMaterial3D_property_detail_enabled>` is
`true`, the `detail_albedo<class_BaseMaterial3D_property_detail_albedo>`
texture is drawn *below* the
`normal_texture<class_BaseMaterial3D_property_normal_texture>`. To
display a normal map *above* the
`detail_albedo<class_BaseMaterial3D_property_detail_albedo>` texture,
use `detail_normal<class_BaseMaterial3D_property_detail_normal>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **orm\_texture**
`🔗<class_BaseMaterial3D_property_orm_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The Occlusion/Roughness/Metallic texture to use. This is a more
efficient replacement of
`ao_texture<class_BaseMaterial3D_property_ao_texture>`,
`roughness_texture<class_BaseMaterial3D_property_roughness_texture>` and
`metallic_texture<class_BaseMaterial3D_property_metallic_texture>` in
`ORMMaterial3D<class_ORMMaterial3D>`. Ambient occlusion is stored in the
red channel. Roughness map is stored in the green channel. Metallic map
is stored in the blue channel. The alpha channel is ignored.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **particles\_anim\_h\_frames**
`🔗<class_BaseMaterial3D_property_particles_anim_h_frames>`

classref-property-setget

-   `void (No return value.)` **set\_particles\_anim\_h\_frames**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_particles\_anim\_h\_frames**()

The number of horizontal frames in the particle sprite sheet. Only
enabled when using
`BILLBOARD_PARTICLES<class_BaseMaterial3D_constant_BILLBOARD_PARTICLES>`.
See `billboard_mode<class_BaseMaterial3D_property_billboard_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **particles\_anim\_loop**
`🔗<class_BaseMaterial3D_property_particles_anim_loop>`

classref-property-setget

-   `void (No return value.)` **set\_particles\_anim\_loop**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_particles\_anim\_loop**()

If `true`, particle animations are looped. Only enabled when using
`BILLBOARD_PARTICLES<class_BaseMaterial3D_constant_BILLBOARD_PARTICLES>`.
See `billboard_mode<class_BaseMaterial3D_property_billboard_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **particles\_anim\_v\_frames**
`🔗<class_BaseMaterial3D_property_particles_anim_v_frames>`

classref-property-setget

-   `void (No return value.)` **set\_particles\_anim\_v\_frames**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_particles\_anim\_v\_frames**()

The number of vertical frames in the particle sprite sheet. Only enabled
when using
`BILLBOARD_PARTICLES<class_BaseMaterial3D_constant_BILLBOARD_PARTICLES>`.
See `billboard_mode<class_BaseMaterial3D_property_billboard_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **point\_size** = `1.0`
`🔗<class_BaseMaterial3D_property_point_size>`

classref-property-setget

-   `void (No return value.)` **set\_point\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_point\_size**()

The point size in pixels. See
`use_point_size<class_BaseMaterial3D_property_use_point_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **proximity\_fade\_distance** = `1.0`
`🔗<class_BaseMaterial3D_property_proximity_fade_distance>`

classref-property-setget

-   `void (No return value.)` **set\_proximity\_fade\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_proximity\_fade\_distance**()

Distance over which the fade effect takes place. The larger the distance
the longer it takes for an object to fade.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **proximity\_fade\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_proximity_fade_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_proximity\_fade\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_proximity\_fade\_enabled**()

If `true`, the proximity fade effect is enabled. The proximity fade
effect fades out each pixel based on its distance to another object.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **refraction\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_refraction_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the refraction effect is enabled. Distorts transparency based
on light from behind the object.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **refraction\_scale** = `0.05`
`🔗<class_BaseMaterial3D_property_refraction_scale>`

classref-property-setget

-   `void (No return value.)` **set\_refraction**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_refraction**()

The strength of the refraction effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **refraction\_texture**
`🔗<class_BaseMaterial3D_property_refraction_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture that controls the strength of the refraction per-pixel.
Multiplied by
`refraction_scale<class_BaseMaterial3D_property_refraction_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**refraction\_texture\_channel** = `0`
`🔗<class_BaseMaterial3D_property_refraction_texture_channel>`

classref-property-setget

-   `void (No return value.)`
    **set\_refraction\_texture\_channel**(value:
    `TextureChannel<enum_BaseMaterial3D_TextureChannel>`)
-   `TextureChannel<enum_BaseMaterial3D_TextureChannel>`
    **get\_refraction\_texture\_channel**()

Specifies the channel of the
`refraction_texture<class_BaseMaterial3D_property_refraction_texture>`
in which the refraction information is stored. This is useful when you
store the information for multiple effects in a single texture. For
example if you stored refraction in the red channel, roughness in the
blue, and ambient occlusion in the green you could reduce the number of
textures you use.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rim** = `1.0`
`🔗<class_BaseMaterial3D_property_rim>`

classref-property-setget

-   `void (No return value.)` **set\_rim**(value: `float<class_float>`)
-   `float<class_float>` **get\_rim**()

Sets the strength of the rim lighting effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **rim\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_rim_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, rim effect is enabled. Rim lighting increases the brightness
at glancing angles on an object.

\*\*Note:\*\* Rim lighting is not visible if the material's
`shading_mode<class_BaseMaterial3D_property_shading_mode>` is
`SHADING_MODE_UNSHADED<class_BaseMaterial3D_constant_SHADING_MODE_UNSHADED>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **rim\_texture**
`🔗<class_BaseMaterial3D_property_rim_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture used to set the strength of the rim lighting effect per-pixel.
Multiplied by `rim<class_BaseMaterial3D_property_rim>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rim\_tint** = `0.5`
`🔗<class_BaseMaterial3D_property_rim_tint>`

classref-property-setget

-   `void (No return value.)` **set\_rim\_tint**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_rim\_tint**()

The amount of to blend light and albedo color when rendering rim effect.
If `0` the light color is used, while `1` means albedo color is used. An
intermediate value generally works best.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **roughness** = `1.0`
`🔗<class_BaseMaterial3D_property_roughness>`

classref-property-setget

-   `void (No return value.)` **set\_roughness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_roughness**()

Surface reflection. A value of `0` represents a perfect mirror while a
value of `1` completely blurs the reflection. See also
`metallic<class_BaseMaterial3D_property_metallic>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **roughness\_texture**
`🔗<class_BaseMaterial3D_property_roughness_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture used to control the roughness per-pixel. Multiplied by
`roughness<class_BaseMaterial3D_property_roughness>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureChannel<enum_BaseMaterial3D_TextureChannel>`
**roughness\_texture\_channel** = `0`
`🔗<class_BaseMaterial3D_property_roughness_texture_channel>`

classref-property-setget

-   `void (No return value.)`
    **set\_roughness\_texture\_channel**(value:
    `TextureChannel<enum_BaseMaterial3D_TextureChannel>`)
-   `TextureChannel<enum_BaseMaterial3D_TextureChannel>`
    **get\_roughness\_texture\_channel**()

Specifies the channel of the
`roughness_texture<class_BaseMaterial3D_property_roughness_texture>` in
which the roughness information is stored. This is useful when you store
the information for multiple effects in a single texture. For example if
you stored metallic in the red channel, roughness in the blue, and
ambient occlusion in the green you could reduce the number of textures
you use.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ShadingMode<enum_BaseMaterial3D_ShadingMode>` **shading\_mode** = `1`
`🔗<class_BaseMaterial3D_property_shading_mode>`

classref-property-setget

-   `void (No return value.)` **set\_shading\_mode**(value:
    `ShadingMode<enum_BaseMaterial3D_ShadingMode>`)
-   `ShadingMode<enum_BaseMaterial3D_ShadingMode>`
    **get\_shading\_mode**()

Sets whether the shading takes place, per-pixel, per-vertex or unshaded.
Per-vertex lighting is faster, making it the best choice for mobile
applications, however it looks considerably worse than per-pixel.
Unshaded rendering is the fastest, but disables all interactions with
lights.

\*\*Note:\*\* Setting the shading mode vertex shading currently has no
effect, as vertex shading is not implemented yet.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shadow\_to\_opacity** = `false`
`🔗<class_BaseMaterial3D_property_shadow_to_opacity>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, enables the "shadow to opacity" render mode where lighting
modifies the alpha so shadowed areas are opaque and non-shadowed areas
are transparent. Useful for overlaying shadows onto a camera feed in AR.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SpecularMode<enum_BaseMaterial3D_SpecularMode>` **specular\_mode** =
`0` `🔗<class_BaseMaterial3D_property_specular_mode>`

classref-property-setget

-   `void (No return value.)` **set\_specular\_mode**(value:
    `SpecularMode<enum_BaseMaterial3D_SpecularMode>`)
-   `SpecularMode<enum_BaseMaterial3D_SpecularMode>`
    **get\_specular\_mode**()

The method for rendering the specular blob. See
`SpecularMode<enum_BaseMaterial3D_SpecularMode>`.

\*\*Note:\*\*
`specular_mode<class_BaseMaterial3D_property_specular_mode>` only
applies to the specular blob. It does not affect specular reflections
from the sky, screen-space reflections, `VoxelGI<class_VoxelGI>`, SDFGI
or `ReflectionProbe<class_ReflectionProbe>`s. To disable reflections
from these sources as well, set
`metallic_specular<class_BaseMaterial3D_property_metallic_specular>` to
`0.0` instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **subsurf\_scatter\_enabled** = `false`
`🔗<class_BaseMaterial3D_property_subsurf_scatter_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, subsurface scattering is enabled. Emulates light that
penetrates an object's surface, is scattered, and then emerges.
Subsurface scattering quality is controlled by
`ProjectSettings.rendering/environment/subsurface_scattering/subsurface_scattering_quality<class_ProjectSettings_property_rendering/environment/subsurface_scattering/subsurface_scattering_quality>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **subsurf\_scatter\_skin\_mode** = `false`
`🔗<class_BaseMaterial3D_property_subsurf_scatter_skin_mode>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, subsurface scattering will use a special mode optimized for
the color and density of human skin, such as boosting the intensity of
the red channel in subsurface scattering.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **subsurf\_scatter\_strength** = `0.0`
`🔗<class_BaseMaterial3D_property_subsurf_scatter_strength>`

classref-property-setget

-   `void (No return value.)`
    **set\_subsurface\_scattering\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_subsurface\_scattering\_strength**()

The strength of the subsurface scattering effect. The depth of the
effect is also controlled by
`ProjectSettings.rendering/environment/subsurface_scattering/subsurface_scattering_scale<class_ProjectSettings_property_rendering/environment/subsurface_scattering/subsurface_scattering_scale>`,
which is set globally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **subsurf\_scatter\_texture**
`🔗<class_BaseMaterial3D_property_subsurf_scatter_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Texture used to control the subsurface scattering strength. Stored in
the red texture channel. Multiplied by
`subsurf_scatter_strength<class_BaseMaterial3D_property_subsurf_scatter_strength>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **subsurf\_scatter\_transmittance\_boost** = `0.0`
`🔗<class_BaseMaterial3D_property_subsurf_scatter_transmittance_boost>`

classref-property-setget

-   `void (No return value.)` **set\_transmittance\_boost**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_transmittance\_boost**()

The intensity of the subsurface scattering transmittance effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **subsurf\_scatter\_transmittance\_color** =
`Color(1, 1, 1, 1)`
`🔗<class_BaseMaterial3D_property_subsurf_scatter_transmittance_color>`

classref-property-setget

-   `void (No return value.)` **set\_transmittance\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_transmittance\_color**()

The color to multiply the subsurface scattering transmittance effect
with. Ignored if
`subsurf_scatter_skin_mode<class_BaseMaterial3D_property_subsurf_scatter_skin_mode>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **subsurf\_scatter\_transmittance\_depth** = `0.1`
`🔗<class_BaseMaterial3D_property_subsurf_scatter_transmittance_depth>`

classref-property-setget

-   `void (No return value.)` **set\_transmittance\_depth**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_transmittance\_depth**()

The depth of the subsurface scattering transmittance effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **subsurf\_scatter\_transmittance\_enabled** =
`false`
`🔗<class_BaseMaterial3D_property_subsurf_scatter_transmittance_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_feature**(feature:
    `Feature<enum_BaseMaterial3D_Feature>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, enables subsurface scattering transmittance. Only effective
if
`subsurf_scatter_enabled<class_BaseMaterial3D_property_subsurf_scatter_enabled>`
is `true`. See also
`backlight_enabled<class_BaseMaterial3D_property_backlight_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>`
**subsurf\_scatter\_transmittance\_texture**
`🔗<class_BaseMaterial3D_property_subsurf_scatter_transmittance_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**(param:
    `TextureParam<enum_BaseMaterial3D_TextureParam>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The texture to use for multiplying the intensity of the subsurface
scattering transmittance intensity. See also
`subsurf_scatter_texture<class_BaseMaterial3D_property_subsurf_scatter_texture>`.
Ignored if
`subsurf_scatter_skin_mode<class_BaseMaterial3D_property_subsurf_scatter_skin_mode>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureFilter<enum_BaseMaterial3D_TextureFilter>` **texture\_filter** =
`3` `🔗<class_BaseMaterial3D_property_texture_filter>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_filter**(value:
    `TextureFilter<enum_BaseMaterial3D_TextureFilter>`)
-   `TextureFilter<enum_BaseMaterial3D_TextureFilter>`
    **get\_texture\_filter**()

Filter flags for the texture. See
`TextureFilter<enum_BaseMaterial3D_TextureFilter>` for options.

\*\*Note:\*\*
`heightmap_texture<class_BaseMaterial3D_property_heightmap_texture>` is
always sampled with linear filtering, even if nearest-neighbor filtering
is selected here. This is to ensure the heightmap effect looks as
intended. If you need sharper height transitions between pixels, resize
the heightmap texture in an image editor with nearest-neighbor
filtering.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **texture\_repeat** = `true`
`🔗<class_BaseMaterial3D_property_texture_repeat>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Repeat flags for the texture. See
`TextureFilter<enum_BaseMaterial3D_TextureFilter>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transparency<enum_BaseMaterial3D_Transparency>` **transparency** = `0`
`🔗<class_BaseMaterial3D_property_transparency>`

classref-property-setget

-   `void (No return value.)` **set\_transparency**(value:
    `Transparency<enum_BaseMaterial3D_Transparency>`)
-   `Transparency<enum_BaseMaterial3D_Transparency>`
    **get\_transparency**()

The material's transparency mode. Some transparency modes will disable
shadow casting. Any transparency mode other than
`TRANSPARENCY_DISABLED<class_BaseMaterial3D_constant_TRANSPARENCY_DISABLED>`
has a greater performance impact compared to opaque rendering. See also
`blend_mode<class_BaseMaterial3D_property_blend_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_particle\_trails** = `false`
`🔗<class_BaseMaterial3D_property_use_particle_trails>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, enables parts of the shader required for
`GPUParticles3D<class_GPUParticles3D>` trails to function. This also
requires using a mesh with appropriate skinning, such as
`RibbonTrailMesh<class_RibbonTrailMesh>` or
`TubeTrailMesh<class_TubeTrailMesh>`. Enabling this feature outside of
materials used in `GPUParticles3D<class_GPUParticles3D>` meshes will
break material rendering.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_point\_size** = `false`
`🔗<class_BaseMaterial3D_property_use_point_size>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, render point size can be changed.

\*\*Note:\*\* This is only effective for objects whose geometry is
point-based rather than triangle-based. See also
`point_size<class_BaseMaterial3D_property_point_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **uv1\_offset** = `Vector3(0, 0, 0)`
`🔗<class_BaseMaterial3D_property_uv1_offset>`

classref-property-setget

-   `void (No return value.)` **set\_uv1\_offset**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_uv1\_offset**()

How much to offset the `UV` coordinates. This amount will be added to
`UV` in the vertex function. This can be used to offset a texture. The Z
component is used when
`uv1_triplanar<class_BaseMaterial3D_property_uv1_triplanar>` is enabled,
but it is not used anywhere else.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **uv1\_scale** = `Vector3(1, 1, 1)`
`🔗<class_BaseMaterial3D_property_uv1_scale>`

classref-property-setget

-   `void (No return value.)` **set\_uv1\_scale**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_uv1\_scale**()

How much to scale the `UV` coordinates. This is multiplied by `UV` in
the vertex function. The Z component is used when
`uv1_triplanar<class_BaseMaterial3D_property_uv1_triplanar>` is enabled,
but it is not used anywhere else.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **uv1\_triplanar** = `false`
`🔗<class_BaseMaterial3D_property_uv1_triplanar>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, instead of using `UV` textures will use a triplanar texture
lookup to determine how to apply textures. Triplanar uses the
orientation of the object's surface to blend between texture
coordinates. It reads from the source texture 3 times, once for each
axis and then blends between the results based on how closely the pixel
aligns with each axis. This is often used for natural features to get a
realistic blend of materials. Because triplanar texturing requires many
more texture reads per-pixel it is much slower than normal UV texturing.
Additionally, because it is blending the texture between the three axes,
it is unsuitable when you are trying to achieve crisp texturing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **uv1\_triplanar\_sharpness** = `1.0`
`🔗<class_BaseMaterial3D_property_uv1_triplanar_sharpness>`

classref-property-setget

-   `void (No return value.)`
    **set\_uv1\_triplanar\_blend\_sharpness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_uv1\_triplanar\_blend\_sharpness**()

A lower number blends the texture more softly while a higher number
blends the texture more sharply.

\*\*Note:\*\*
`uv1_triplanar_sharpness<class_BaseMaterial3D_property_uv1_triplanar_sharpness>`
is clamped between `0.0` and `150.0` (inclusive) as values outside that
range can look broken depending on the mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **uv1\_world\_triplanar** = `false`
`🔗<class_BaseMaterial3D_property_uv1_world_triplanar>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, triplanar mapping for `UV` is calculated in world space
rather than object local space. See also
`uv1_triplanar<class_BaseMaterial3D_property_uv1_triplanar>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **uv2\_offset** = `Vector3(0, 0, 0)`
`🔗<class_BaseMaterial3D_property_uv2_offset>`

classref-property-setget

-   `void (No return value.)` **set\_uv2\_offset**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_uv2\_offset**()

How much to offset the `UV2` coordinates. This amount will be added to
`UV2` in the vertex function. This can be used to offset a texture. The
Z component is used when
`uv2_triplanar<class_BaseMaterial3D_property_uv2_triplanar>` is enabled,
but it is not used anywhere else.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **uv2\_scale** = `Vector3(1, 1, 1)`
`🔗<class_BaseMaterial3D_property_uv2_scale>`

classref-property-setget

-   `void (No return value.)` **set\_uv2\_scale**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_uv2\_scale**()

How much to scale the `UV2` coordinates. This is multiplied by `UV2` in
the vertex function. The Z component is used when
`uv2_triplanar<class_BaseMaterial3D_property_uv2_triplanar>` is enabled,
but it is not used anywhere else.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **uv2\_triplanar** = `false`
`🔗<class_BaseMaterial3D_property_uv2_triplanar>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, instead of using `UV2` textures will use a triplanar texture
lookup to determine how to apply textures. Triplanar uses the
orientation of the object's surface to blend between texture
coordinates. It reads from the source texture 3 times, once for each
axis and then blends between the results based on how closely the pixel
aligns with each axis. This is often used for natural features to get a
realistic blend of materials. Because triplanar texturing requires many
more texture reads per-pixel it is much slower than normal UV texturing.
Additionally, because it is blending the texture between the three axes,
it is unsuitable when you are trying to achieve crisp texturing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **uv2\_triplanar\_sharpness** = `1.0`
`🔗<class_BaseMaterial3D_property_uv2_triplanar_sharpness>`

classref-property-setget

-   `void (No return value.)`
    **set\_uv2\_triplanar\_blend\_sharpness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_uv2\_triplanar\_blend\_sharpness**()

A lower number blends the texture more softly while a higher number
blends the texture more sharply.

\*\*Note:\*\*
`uv2_triplanar_sharpness<class_BaseMaterial3D_property_uv2_triplanar_sharpness>`
is clamped between `0.0` and `150.0` (inclusive) as values outside that
range can look broken depending on the mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **uv2\_world\_triplanar** = `false`
`🔗<class_BaseMaterial3D_property_uv2_world_triplanar>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, triplanar mapping for `UV2` is calculated in world space
rather than object local space. See also
`uv2_triplanar<class_BaseMaterial3D_property_uv2_triplanar>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **vertex\_color\_is\_srgb** = `false`
`🔗<class_BaseMaterial3D_property_vertex_color_is_srgb>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, vertex colors are considered to be stored in sRGB color space
and are converted to linear color space during rendering. If `false`,
vertex colors are considered to be stored in linear color space and are
rendered as-is. See also
`albedo_texture_force_srgb<class_BaseMaterial3D_property_albedo_texture_force_srgb>`.

\*\*Note:\*\* Only effective when using the Forward+ and Mobile
rendering methods, not Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **vertex\_color\_use\_as\_albedo** = `false`
`🔗<class_BaseMaterial3D_property_vertex_color_use_as_albedo>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag:
    `Flags<enum_BaseMaterial3D_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the vertex color is used as albedo color.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **get\_feature**(feature:
`Feature<enum_BaseMaterial3D_Feature>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_BaseMaterial3D_method_get_feature>`

Returns `true`, if the specified `Feature<enum_BaseMaterial3D_Feature>`
is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_flag**(flag:
`Flags<enum_BaseMaterial3D_Flags>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_BaseMaterial3D_method_get_flag>`

Returns `true`, if the specified flag is enabled. See
`Flags<enum_BaseMaterial3D_Flags>` enumerator for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_texture**(param:
`TextureParam<enum_BaseMaterial3D_TextureParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_BaseMaterial3D_method_get_texture>`

Returns the `Texture2D<class_Texture2D>` associated with the specified
`TextureParam<enum_BaseMaterial3D_TextureParam>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_feature**(feature:
`Feature<enum_BaseMaterial3D_Feature>`, enable: `bool<class_bool>`)
`🔗<class_BaseMaterial3D_method_set_feature>`

If `true`, enables the specified `Feature<enum_BaseMaterial3D_Feature>`.
Many features that are available in **BaseMaterial3D**s need to be
enabled before use. This way the cost for using the feature is only
incurred when specified. Features can also be enabled by setting the
corresponding member to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_flag**(flag:
`Flags<enum_BaseMaterial3D_Flags>`, enable: `bool<class_bool>`)
`🔗<class_BaseMaterial3D_method_set_flag>`

If `true`, enables the specified flag. Flags are optional behavior that
can be turned on and off. Only one flag can be enabled at a time with
this function, the flag enumerators cannot be bit-masked together to
enable or disable multiple flags at once. Flags can also be enabled by
setting the corresponding member to `true`. See
`Flags<enum_BaseMaterial3D_Flags>` enumerator for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_texture**(param:
`TextureParam<enum_BaseMaterial3D_TextureParam>`, texture:
`Texture2D<class_Texture2D>`)
`🔗<class_BaseMaterial3D_method_set_texture>`

Sets the texture for the slot specified by `param`. See
`TextureParam<enum_BaseMaterial3D_TextureParam>` for available slots.
