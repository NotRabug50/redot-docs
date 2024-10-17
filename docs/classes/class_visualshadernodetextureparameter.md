github\_url  
hide

# VisualShaderNodeTextureParameter

**Inherits:**
`VisualShaderNodeParameter<class_VisualShaderNodeParameter>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeCubemapParameter<class_VisualShaderNodeCubemapParameter>`,
`VisualShaderNodeTexture2DArrayParameter<class_VisualShaderNodeTexture2DArrayParameter>`,
`VisualShaderNodeTexture2DParameter<class_VisualShaderNodeTexture2DParameter>`,
`VisualShaderNodeTexture3DParameter<class_VisualShaderNodeTexture3DParameter>`,
`VisualShaderNodeTextureParameterTriplanar<class_VisualShaderNodeTextureParameterTriplanar>`

Performs a uniform texture lookup within the visual shader graph.

classref-introduction-group

## Description

Performs a lookup operation on the texture provided as a uniform for the
shader.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TextureType**:
`🔗<enum_VisualShaderNodeTextureParameter_TextureType>`

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTextureParameter_TextureType>`
**TYPE\_DATA** = `0`

No hints are added to the uniform declaration.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTextureParameter_TextureType>`
**TYPE\_COLOR** = `1`

Adds `source_color` as hint to the uniform declaration for proper sRGB
to linear conversion.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTextureParameter_TextureType>`
**TYPE\_NORMAL\_MAP** = `2`

Adds `hint_normal` as hint to the uniform declaration, which internally
converts the texture for proper usage as normal map.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTextureParameter_TextureType>`
**TYPE\_ANISOTROPY** = `3`

Adds `hint_anisotropy` as hint to the uniform declaration to use for a
flowmap.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTextureParameter_TextureType>`
**TYPE\_MAX** = `4`

Represents the size of the
`TextureType<enum_VisualShaderNodeTextureParameter_TextureType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ColorDefault**:
`🔗<enum_VisualShaderNodeTextureParameter_ColorDefault>`

classref-enumeration-constant

`ColorDefault<enum_VisualShaderNodeTextureParameter_ColorDefault>`
**COLOR\_DEFAULT\_WHITE** = `0`

Defaults to fully opaque white color.

classref-enumeration-constant

`ColorDefault<enum_VisualShaderNodeTextureParameter_ColorDefault>`
**COLOR\_DEFAULT\_BLACK** = `1`

Defaults to fully opaque black color.

classref-enumeration-constant

`ColorDefault<enum_VisualShaderNodeTextureParameter_ColorDefault>`
**COLOR\_DEFAULT\_TRANSPARENT** = `2`

Defaults to fully transparent black color.

classref-enumeration-constant

`ColorDefault<enum_VisualShaderNodeTextureParameter_ColorDefault>`
**COLOR\_DEFAULT\_MAX** = `3`

Represents the size of the
`ColorDefault<enum_VisualShaderNodeTextureParameter_ColorDefault>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureFilter**:
`🔗<enum_VisualShaderNodeTextureParameter_TextureFilter>`

classref-enumeration-constant

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**FILTER\_DEFAULT** = `0`

Sample the texture using the filter determined by the node this shader
is attached to.

classref-enumeration-constant

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**FILTER\_NEAREST** = `1`

The texture filter reads from the nearest pixel only. This makes the
texture look pixelated from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**FILTER\_LINEAR** = `2`

The texture filter blends between the nearest 4 pixels. This makes the
texture look smooth from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**FILTER\_NEAREST\_MIPMAP** = `3`

The texture filter reads from the nearest pixel and blends between the
nearest 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`). This makes the texture look pixelated from up close, and
smooth from a distance.

Use this for non-pixel art textures that may be viewed at a low scale
(e.g. due to `Camera2D<class_Camera2D>` zoom or sprite scaling), as
mipmaps are important to smooth out pixels that are smaller than
on-screen pixels.

classref-enumeration-constant

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**FILTER\_LINEAR\_MIPMAP** = `4`

The texture filter blends between the nearest 4 pixels and between the
nearest 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`). This makes the texture look smooth from up close, and smooth
from a distance.

Use this for non-pixel art textures that may be viewed at a low scale
(e.g. due to `Camera2D<class_Camera2D>` zoom or sprite scaling), as
mipmaps are important to smooth out pixels that are smaller than
on-screen pixels.

classref-enumeration-constant

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**FILTER\_NEAREST\_MIPMAP\_ANISOTROPIC** = `5`

The texture filter reads from the nearest pixel and blends between 2
mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`) based on the angle between the surface and the camera view.
This makes the texture look pixelated from up close, and smooth from a
distance. Anisotropic filtering improves texture quality on surfaces
that are almost in line with the camera, but is slightly slower. The
anisotropic filtering level can be changed by adjusting
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

\*\*Note:\*\* This texture filter is rarely useful in 2D projects.
`FILTER_NEAREST_MIPMAP<class_VisualShaderNodeTextureParameter_constant_FILTER_NEAREST_MIPMAP>`
is usually more appropriate in this case.

classref-enumeration-constant

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**FILTER\_LINEAR\_MIPMAP\_ANISOTROPIC** = `6`

The texture filter blends between the nearest 4 pixels and blends
between 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`) based on the angle between the surface and the camera view.
This makes the texture look smooth from up close, and smooth from a
distance. Anisotropic filtering improves texture quality on surfaces
that are almost in line with the camera, but is slightly slower. The
anisotropic filtering level can be changed by adjusting
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

\*\*Note:\*\* This texture filter is rarely useful in 2D projects.
`FILTER_LINEAR_MIPMAP<class_VisualShaderNodeTextureParameter_constant_FILTER_LINEAR_MIPMAP>`
is usually more appropriate in this case.

classref-enumeration-constant

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**FILTER\_MAX** = `7`

Represents the size of the
`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureRepeat**:
`🔗<enum_VisualShaderNodeTextureParameter_TextureRepeat>`

classref-enumeration-constant

`TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>`
**REPEAT\_DEFAULT** = `0`

Sample the texture using the repeat mode determined by the node this
shader is attached to.

classref-enumeration-constant

`TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>`
**REPEAT\_ENABLED** = `1`

Texture will repeat normally.

classref-enumeration-constant

`TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>`
**REPEAT\_DISABLED** = `2`

Texture will not repeat.

classref-enumeration-constant

`TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>`
**REPEAT\_MAX** = `3`

Represents the size of the
`TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureSource**:
`🔗<enum_VisualShaderNodeTextureParameter_TextureSource>`

classref-enumeration-constant

`TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`
**SOURCE\_NONE** = `0`

The texture source is not specified in the shader.

classref-enumeration-constant

`TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`
**SOURCE\_SCREEN** = `1`

The texture source is the screen texture which captures all opaque
objects drawn this frame.

classref-enumeration-constant

`TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`
**SOURCE\_DEPTH** = `2`

The texture source is the depth texture from the depth prepass.

classref-enumeration-constant

`TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`
**SOURCE\_NORMAL\_ROUGHNESS** = `3`

The texture source is the normal-roughness buffer from the depth
prepass.

classref-enumeration-constant

`TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`
**SOURCE\_MAX** = `4`

Represents the size of the
`TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`ColorDefault<enum_VisualShaderNodeTextureParameter_ColorDefault>`
**color\_default** = `0`
`🔗<class_VisualShaderNodeTextureParameter_property_color_default>`

classref-property-setget

-   `void (No return value.)` **set\_color\_default**(value:
    `ColorDefault<enum_VisualShaderNodeTextureParameter_ColorDefault>`)
-   `ColorDefault<enum_VisualShaderNodeTextureParameter_ColorDefault>`
    **get\_color\_default**()

Sets the default color if no texture is assigned to the uniform.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
**texture\_filter** = `0`
`🔗<class_VisualShaderNodeTextureParameter_property_texture_filter>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_filter**(value:
    `TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`)
-   `TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>`
    **get\_texture\_filter**()

Sets the texture filtering mode. See
`TextureFilter<enum_VisualShaderNodeTextureParameter_TextureFilter>` for
options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>`
**texture\_repeat** = `0`
`🔗<class_VisualShaderNodeTextureParameter_property_texture_repeat>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_repeat**(value:
    `TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>`)
-   `TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>`
    **get\_texture\_repeat**()

Sets the texture repeating mode. See
`TextureRepeat<enum_VisualShaderNodeTextureParameter_TextureRepeat>` for
options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`
**texture\_source** = `0`
`🔗<class_VisualShaderNodeTextureParameter_property_texture_source>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_source**(value:
    `TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`)
-   `TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>`
    **get\_texture\_source**()

Sets the texture source mode. Used for reading from the screen, depth,
or normal\_roughness texture. See
`TextureSource<enum_VisualShaderNodeTextureParameter_TextureSource>` for
options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureType<enum_VisualShaderNodeTextureParameter_TextureType>`
**texture\_type** = `0`
`🔗<class_VisualShaderNodeTextureParameter_property_texture_type>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_type**(value:
    `TextureType<enum_VisualShaderNodeTextureParameter_TextureType>`)
-   `TextureType<enum_VisualShaderNodeTextureParameter_TextureType>`
    **get\_texture\_type**()

Defines the type of data provided by the source texture. See
`TextureType<enum_VisualShaderNodeTextureParameter_TextureType>` for
options.
