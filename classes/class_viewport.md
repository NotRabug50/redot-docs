github\_url  
hide

# Viewport

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `SubViewport<class_SubViewport>`,
`Window<class_Window>`

Abstract base class for viewports. Encapsulates drawing and interaction
with a game world.

classref-introduction-group

## Description

A **Viewport** creates a different view into the screen, or a sub-view
inside another viewport. Child 2D nodes will display on it, and child
Camera3D 3D nodes will render on it too.

Optionally, a viewport can have its own 2D or 3D world, so it doesn't
share what it draws with other viewports.

Viewports can also choose to be audio listeners, so they generate
positional audio depending on a 2D or 3D camera child of it.

Also, viewports can be assigned to different screens in case the devices
have multiple screens.

Finally, viewports can also behave as render targets, in which case they
will not be visible unless the associated texture is used to draw.

classref-introduction-group

## Tutorials

-   `Using Viewports <../tutorials/rendering/viewports>`
-   `Viewport and canvas transforms <../tutorials/2d/2d_transforms>`
-   [GUI in 3D Viewport
    Demo](https://godotengine.org/asset-library/asset/2807)
-   [3D in 2D Viewport
    Demo](https://godotengine.org/asset-library/asset/2804)
-   [2D in 3D Viewport
    Demo](https://godotengine.org/asset-library/asset/2803)
-   [Screen Capture
    Demo](https://godotengine.org/asset-library/asset/2808)
-   [Dynamic Split Screen
    Demo](https://godotengine.org/asset-library/asset/2806)
-   [3D Resolution Scaling
    Demo](https://godotengine.org/asset-library/asset/2805)

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**gui\_focus\_changed**(node: `Control<class_Control>`)
`🔗<class_Viewport_signal_gui_focus_changed>`

Emitted when a Control node grabs keyboard focus.

\*\*Note:\*\* A Control node losing focus doesn't cause this signal to
be emitted.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**size\_changed**() `🔗<class_Viewport_signal_size_changed>`

Emitted when the size of the viewport is changed, whether by resizing of
window, or some other means.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **PositionalShadowAtlasQuadrantSubdiv**:
`🔗<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`

classref-enumeration-constant

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**SHADOW\_ATLAS\_QUADRANT\_SUBDIV\_DISABLED** = `0`

This quadrant will not be used.

classref-enumeration-constant

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**SHADOW\_ATLAS\_QUADRANT\_SUBDIV\_1** = `1`

This quadrant will only be used by one shadow map.

classref-enumeration-constant

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**SHADOW\_ATLAS\_QUADRANT\_SUBDIV\_4** = `2`

This quadrant will be split in 4 and used by up to 4 shadow maps.

classref-enumeration-constant

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**SHADOW\_ATLAS\_QUADRANT\_SUBDIV\_16** = `3`

This quadrant will be split 16 ways and used by up to 16 shadow maps.

classref-enumeration-constant

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**SHADOW\_ATLAS\_QUADRANT\_SUBDIV\_64** = `4`

This quadrant will be split 64 ways and used by up to 64 shadow maps.

classref-enumeration-constant

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**SHADOW\_ATLAS\_QUADRANT\_SUBDIV\_256** = `5`

This quadrant will be split 256 ways and used by up to 256 shadow maps.
Unless the
`positional_shadow_atlas_size<class_Viewport_property_positional_shadow_atlas_size>`
is very high, the shadows in this quadrant will be very low resolution.

classref-enumeration-constant

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**SHADOW\_ATLAS\_QUADRANT\_SUBDIV\_1024** = `6`

This quadrant will be split 1024 ways and used by up to 1024 shadow
maps. Unless the
`positional_shadow_atlas_size<class_Viewport_property_positional_shadow_atlas_size>`
is very high, the shadows in this quadrant will be very low resolution.

classref-enumeration-constant

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**SHADOW\_ATLAS\_QUADRANT\_SUBDIV\_MAX** = `7`

Represents the size of the
`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Scaling3DMode**: `🔗<enum_Viewport_Scaling3DMode>`

classref-enumeration-constant

`Scaling3DMode<enum_Viewport_Scaling3DMode>`
**SCALING\_3D\_MODE\_BILINEAR** = `0`

Use bilinear scaling for the viewport's 3D buffer. The amount of scaling
can be set using
`scaling_3d_scale<class_Viewport_property_scaling_3d_scale>`. Values
less than `1.0` will result in undersampling while values greater than
`1.0` will result in supersampling. A value of `1.0` disables scaling.

classref-enumeration-constant

`Scaling3DMode<enum_Viewport_Scaling3DMode>` **SCALING\_3D\_MODE\_FSR**
= `1`

Use AMD FidelityFX Super Resolution 1.0 upscaling for the viewport's 3D
buffer. The amount of scaling can be set using
`scaling_3d_scale<class_Viewport_property_scaling_3d_scale>`. Values
less than `1.0` will be result in the viewport being upscaled using FSR.
Values greater than `1.0` are not supported and bilinear downsampling
will be used instead. A value of `1.0` disables scaling.

classref-enumeration-constant

`Scaling3DMode<enum_Viewport_Scaling3DMode>` **SCALING\_3D\_MODE\_FSR2**
= `2`

Use AMD FidelityFX Super Resolution 2.2 upscaling for the viewport's 3D
buffer. The amount of scaling can be set using
`scaling_3d_scale<class_Viewport_property_scaling_3d_scale>`. Values
less than `1.0` will be result in the viewport being upscaled using
FSR2. Values greater than `1.0` are not supported and bilinear
downsampling will be used instead. A value of `1.0` will use FSR2 at
native resolution as a TAA solution.

classref-enumeration-constant

`Scaling3DMode<enum_Viewport_Scaling3DMode>` **SCALING\_3D\_MODE\_MAX**
= `3`

Represents the size of the `Scaling3DMode<enum_Viewport_Scaling3DMode>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MSAA**: `🔗<enum_Viewport_MSAA>`

classref-enumeration-constant

`MSAA<enum_Viewport_MSAA>` **MSAA\_DISABLED** = `0`

Multisample antialiasing mode disabled. This is the default value, and
is also the fastest setting.

classref-enumeration-constant

`MSAA<enum_Viewport_MSAA>` **MSAA\_2X** = `1`

Use 2× Multisample Antialiasing. This has a moderate performance cost.
It helps reduce aliasing noticeably, but 4× MSAA still looks
substantially better.

classref-enumeration-constant

`MSAA<enum_Viewport_MSAA>` **MSAA\_4X** = `2`

Use 4× Multisample Antialiasing. This has a significant performance
cost, and is generally a good compromise between performance and
quality.

classref-enumeration-constant

`MSAA<enum_Viewport_MSAA>` **MSAA\_8X** = `3`

Use 8× Multisample Antialiasing. This has a very high performance cost.
The difference between 4× and 8× MSAA may not always be visible in real
gameplay conditions. Likely unsupported on low-end and older hardware.

classref-enumeration-constant

`MSAA<enum_Viewport_MSAA>` **MSAA\_MAX** = `4`

Represents the size of the `MSAA<enum_Viewport_MSAA>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ScreenSpaceAA**: `🔗<enum_Viewport_ScreenSpaceAA>`

classref-enumeration-constant

`ScreenSpaceAA<enum_Viewport_ScreenSpaceAA>`
**SCREEN\_SPACE\_AA\_DISABLED** = `0`

Do not perform any antialiasing in the full screen post-process.

classref-enumeration-constant

`ScreenSpaceAA<enum_Viewport_ScreenSpaceAA>` **SCREEN\_SPACE\_AA\_FXAA**
= `1`

Use fast approximate antialiasing. FXAA is a popular screen-space
antialiasing method, which is fast but will make the image look blurry,
especially at lower resolutions. It can still work relatively well at
large resolutions such as 1440p and 4K.

classref-enumeration-constant

`ScreenSpaceAA<enum_Viewport_ScreenSpaceAA>` **SCREEN\_SPACE\_AA\_MAX**
= `2`

Represents the size of the `ScreenSpaceAA<enum_Viewport_ScreenSpaceAA>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **RenderInfo**: `🔗<enum_Viewport_RenderInfo>`

classref-enumeration-constant

`RenderInfo<enum_Viewport_RenderInfo>`
**RENDER\_INFO\_OBJECTS\_IN\_FRAME** = `0`

Amount of objects in frame.

classref-enumeration-constant

`RenderInfo<enum_Viewport_RenderInfo>`
**RENDER\_INFO\_PRIMITIVES\_IN\_FRAME** = `1`

Amount of vertices in frame.

classref-enumeration-constant

`RenderInfo<enum_Viewport_RenderInfo>`
**RENDER\_INFO\_DRAW\_CALLS\_IN\_FRAME** = `2`

Amount of draw calls in frame.

classref-enumeration-constant

`RenderInfo<enum_Viewport_RenderInfo>` **RENDER\_INFO\_MAX** = `3`

Represents the size of the `RenderInfo<enum_Viewport_RenderInfo>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **RenderInfoType**: `🔗<enum_Viewport_RenderInfoType>`

classref-enumeration-constant

`RenderInfoType<enum_Viewport_RenderInfoType>`
**RENDER\_INFO\_TYPE\_VISIBLE** = `0`

Visible render pass (excluding shadows).

classref-enumeration-constant

`RenderInfoType<enum_Viewport_RenderInfoType>`
**RENDER\_INFO\_TYPE\_SHADOW** = `1`

Shadow render pass. Objects will be rendered several times depending on
the number of amounts of lights with shadows and the number of
directional shadow splits.

classref-enumeration-constant

`RenderInfoType<enum_Viewport_RenderInfoType>`
**RENDER\_INFO\_TYPE\_CANVAS** = `2`

Canvas item rendering. This includes all 2D rendering.

classref-enumeration-constant

`RenderInfoType<enum_Viewport_RenderInfoType>`
**RENDER\_INFO\_TYPE\_MAX** = `3`

Represents the size of the
`RenderInfoType<enum_Viewport_RenderInfoType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DebugDraw**: `🔗<enum_Viewport_DebugDraw>`

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_DISABLED** = `0`

Objects are displayed normally.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_UNSHADED** = `1`

Objects are displayed without light information.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_LIGHTING** = `2`

Objects are displayed without textures and only with lighting
information.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_OVERDRAW** = `3`

Objects are displayed semi-transparent with additive blending so you can
see where they are drawing over top of one another. A higher overdraw
means you are wasting performance on drawing pixels that are being
hidden behind others.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_WIREFRAME** = `4`

Objects are displayed as wireframe models.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_NORMAL\_BUFFER** =
`5`

Objects are displayed without lighting information and their textures
replaced by normal mapping.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_VOXEL\_GI\_ALBEDO**
= `6`

Objects are displayed with only the albedo value from
`VoxelGI<class_VoxelGI>`s.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>`
**DEBUG\_DRAW\_VOXEL\_GI\_LIGHTING** = `7`

Objects are displayed with only the lighting value from
`VoxelGI<class_VoxelGI>`s.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>`
**DEBUG\_DRAW\_VOXEL\_GI\_EMISSION** = `8`

Objects are displayed with only the emission color from
`VoxelGI<class_VoxelGI>`s.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_SHADOW\_ATLAS** =
`9`

Draws the shadow atlas that stores shadows from
`OmniLight3D<class_OmniLight3D>`s and `SpotLight3D<class_SpotLight3D>`s
in the upper left quadrant of the **Viewport**.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>`
**DEBUG\_DRAW\_DIRECTIONAL\_SHADOW\_ATLAS** = `10`

Draws the shadow atlas that stores shadows from
`DirectionalLight3D<class_DirectionalLight3D>`s in the upper left
quadrant of the **Viewport**.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_SCENE\_LUMINANCE** =
`11`

Draws the scene luminance buffer (if available) in the upper left
quadrant of the **Viewport**.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_SSAO** = `12`

Draws the screen-space ambient occlusion texture instead of the scene so
that you can clearly see how it is affecting objects. In order for this
display mode to work, you must have
`Environment.ssao_enabled<class_Environment_property_ssao_enabled>` set
in your `WorldEnvironment<class_WorldEnvironment>`.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_SSIL** = `13`

Draws the screen-space indirect lighting texture instead of the scene so
that you can clearly see how it is affecting objects. In order for this
display mode to work, you must have
`Environment.ssil_enabled<class_Environment_property_ssil_enabled>` set
in your `WorldEnvironment<class_WorldEnvironment>`.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_PSSM\_SPLITS** =
`14`

Colors each PSSM split for the
`DirectionalLight3D<class_DirectionalLight3D>`s in the scene a different
color so you can see where the splits are. In order, they will be
colored red, green, blue, and yellow.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_DECAL\_ATLAS** =
`15`

Draws the decal atlas used by `Decal<class_Decal>`s and light projector
textures in the upper left quadrant of the **Viewport**.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_SDFGI** = `16`

Draws the cascades used to render signed distance field global
illumination (SDFGI).

Does nothing if the current environment's
`Environment.sdfgi_enabled<class_Environment_property_sdfgi_enabled>` is
`false` or SDFGI is not supported on the platform.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_SDFGI\_PROBES** =
`17`

Draws the probes used for signed distance field global illumination
(SDFGI).

Does nothing if the current environment's
`Environment.sdfgi_enabled<class_Environment_property_sdfgi_enabled>` is
`false` or SDFGI is not supported on the platform.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_GI\_BUFFER** = `18`

Draws the buffer used for global illumination (GI).

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_DISABLE\_LOD** =
`19`

Draws all of the objects at their highest polycount, without low level
of detail (LOD).

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>`
**DEBUG\_DRAW\_CLUSTER\_OMNI\_LIGHTS** = `20`

Draws the cluster used by `OmniLight3D<class_OmniLight3D>` nodes to
optimize light rendering.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>`
**DEBUG\_DRAW\_CLUSTER\_SPOT\_LIGHTS** = `21`

Draws the cluster used by `SpotLight3D<class_SpotLight3D>` nodes to
optimize light rendering.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_CLUSTER\_DECALS** =
`22`

Draws the cluster used by `Decal<class_Decal>` nodes to optimize decal
rendering.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>`
**DEBUG\_DRAW\_CLUSTER\_REFLECTION\_PROBES** = `23`

Draws the cluster used by `ReflectionProbe<class_ReflectionProbe>` nodes
to optimize decal rendering.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_OCCLUDERS** = `24`

Draws the buffer used for occlusion culling.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_MOTION\_VECTORS** =
`25`

Draws vector lines over the viewport to indicate the movement of pixels
between frames.

classref-enumeration-constant

`DebugDraw<enum_Viewport_DebugDraw>` **DEBUG\_DRAW\_INTERNAL\_BUFFER** =
`26`

Draws the internal resolution buffer of the scene before post-processing
is applied.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DefaultCanvasItemTextureFilter**:
`🔗<enum_Viewport_DefaultCanvasItemTextureFilter>`

classref-enumeration-constant

`DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_FILTER\_NEAREST** = `0`

The texture filter reads from the nearest pixel only. This makes the
texture look pixelated from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_FILTER\_LINEAR** = `1`

The texture filter blends between the nearest 4 pixels. This makes the
texture look smooth from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_FILTER\_LINEAR\_WITH\_MIPMAPS** = `2`

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

`DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_FILTER\_NEAREST\_WITH\_MIPMAPS** = `3`

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

`DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_FILTER\_MAX** = `4`

Represents the size of the
`DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DefaultCanvasItemTextureRepeat**:
`🔗<enum_Viewport_DefaultCanvasItemTextureRepeat>`

classref-enumeration-constant

`DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_REPEAT\_DISABLED** = `0`

Disables textures repeating. Instead, when reading UVs outside the 0-1
range, the value will be clamped to the edge of the texture, resulting
in a stretched out look at the borders of the texture.

classref-enumeration-constant

`DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_REPEAT\_ENABLED** = `1`

Enables the texture to repeat when UV coordinates are outside the 0-1
range. If using one of the linear filtering modes, this can result in
artifacts at the edges of a texture when the sampler filters across the
edges of the texture.

classref-enumeration-constant

`DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_REPEAT\_MIRROR** = `2`

Flip the texture when repeating so that the edge lines up instead of
abruptly changing.

classref-enumeration-constant

`DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`
**DEFAULT\_CANVAS\_ITEM\_TEXTURE\_REPEAT\_MAX** = `3`

Represents the size of the
`DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SDFOversize**: `🔗<enum_Viewport_SDFOversize>`

classref-enumeration-constant

`SDFOversize<enum_Viewport_SDFOversize>` **SDF\_OVERSIZE\_100\_PERCENT**
= `0`

The signed distance field only covers the viewport's own rectangle.

classref-enumeration-constant

`SDFOversize<enum_Viewport_SDFOversize>` **SDF\_OVERSIZE\_120\_PERCENT**
= `1`

The signed distance field is expanded to cover 20% of the viewport's
size around the borders.

classref-enumeration-constant

`SDFOversize<enum_Viewport_SDFOversize>` **SDF\_OVERSIZE\_150\_PERCENT**
= `2`

The signed distance field is expanded to cover 50% of the viewport's
size around the borders.

classref-enumeration-constant

`SDFOversize<enum_Viewport_SDFOversize>` **SDF\_OVERSIZE\_200\_PERCENT**
= `3`

The signed distance field is expanded to cover 100% (double) of the
viewport's size around the borders.

classref-enumeration-constant

`SDFOversize<enum_Viewport_SDFOversize>` **SDF\_OVERSIZE\_MAX** = `4`

Represents the size of the `SDFOversize<enum_Viewport_SDFOversize>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SDFScale**: `🔗<enum_Viewport_SDFScale>`

classref-enumeration-constant

`SDFScale<enum_Viewport_SDFScale>` **SDF\_SCALE\_100\_PERCENT** = `0`

The signed distance field is rendered at full resolution.

classref-enumeration-constant

`SDFScale<enum_Viewport_SDFScale>` **SDF\_SCALE\_50\_PERCENT** = `1`

The signed distance field is rendered at half the resolution of this
viewport.

classref-enumeration-constant

`SDFScale<enum_Viewport_SDFScale>` **SDF\_SCALE\_25\_PERCENT** = `2`

The signed distance field is rendered at a quarter the resolution of
this viewport.

classref-enumeration-constant

`SDFScale<enum_Viewport_SDFScale>` **SDF\_SCALE\_MAX** = `3`

Represents the size of the `SDFScale<enum_Viewport_SDFScale>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VRSMode**: `🔗<enum_Viewport_VRSMode>`

classref-enumeration-constant

`VRSMode<enum_Viewport_VRSMode>` **VRS\_DISABLED** = `0`

Variable Rate Shading is disabled.

classref-enumeration-constant

`VRSMode<enum_Viewport_VRSMode>` **VRS\_TEXTURE** = `1`

Variable Rate Shading uses a texture. Note, for stereoscopic use a
texture atlas with a texture for each view.

classref-enumeration-constant

`VRSMode<enum_Viewport_VRSMode>` **VRS\_XR** = `2`

Variable Rate Shading's texture is supplied by the primary
`XRInterface<class_XRInterface>`.

classref-enumeration-constant

`VRSMode<enum_Viewport_VRSMode>` **VRS\_MAX** = `3`

Represents the size of the `VRSMode<enum_Viewport_VRSMode>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VRSUpdateMode**: `🔗<enum_Viewport_VRSUpdateMode>`

classref-enumeration-constant

`VRSUpdateMode<enum_Viewport_VRSUpdateMode>` **VRS\_UPDATE\_DISABLED** =
`0`

The input texture for variable rate shading will not be processed.

classref-enumeration-constant

`VRSUpdateMode<enum_Viewport_VRSUpdateMode>` **VRS\_UPDATE\_ONCE** = `1`

The input texture for variable rate shading will be processed once.

classref-enumeration-constant

`VRSUpdateMode<enum_Viewport_VRSUpdateMode>` **VRS\_UPDATE\_ALWAYS** =
`2`

The input texture for variable rate shading will be processed each
frame.

classref-enumeration-constant

`VRSUpdateMode<enum_Viewport_VRSUpdateMode>` **VRS\_UPDATE\_MAX** = `3`

Represents the size of the `VRSUpdateMode<enum_Viewport_VRSUpdateMode>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **audio\_listener\_enable\_2d** = `false`
`🔗<class_Viewport_property_audio_listener_enable_2d>`

classref-property-setget

-   `void (No return value.)` **set\_as\_audio\_listener\_2d**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_audio\_listener\_2d**()

If `true`, the viewport will process 2D audio streams.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **audio\_listener\_enable\_3d** = `false`
`🔗<class_Viewport_property_audio_listener_enable_3d>`

classref-property-setget

-   `void (No return value.)` **set\_as\_audio\_listener\_3d**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_audio\_listener\_3d**()

If `true`, the viewport will process 3D audio streams.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **canvas\_cull\_mask** = `4294967295`
`🔗<class_Viewport_property_canvas_cull_mask>`

classref-property-setget

-   `void (No return value.)` **set\_canvas\_cull\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_canvas\_cull\_mask**()

The rendering layers in which this **Viewport** renders
`CanvasItem<class_CanvasItem>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
**canvas\_item\_default\_texture\_filter** = `1`
`🔗<class_Viewport_property_canvas_item_default_texture_filter>`

classref-property-setget

-   `void (No return value.)`
    **set\_default\_canvas\_item\_texture\_filter**(value:
    `DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`)
-   `DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
    **get\_default\_canvas\_item\_texture\_filter**()

Sets the default filter mode used by `CanvasItem<class_CanvasItem>`s in
this Viewport. See
`DefaultCanvasItemTextureFilter<enum_Viewport_DefaultCanvasItemTextureFilter>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`
**canvas\_item\_default\_texture\_repeat** = `0`
`🔗<class_Viewport_property_canvas_item_default_texture_repeat>`

classref-property-setget

-   `void (No return value.)`
    **set\_default\_canvas\_item\_texture\_repeat**(value:
    `DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`)
-   `DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`
    **get\_default\_canvas\_item\_texture\_repeat**()

Sets the default repeat mode used by `CanvasItem<class_CanvasItem>`s in
this Viewport. See
`DefaultCanvasItemTextureRepeat<enum_Viewport_DefaultCanvasItemTextureRepeat>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **canvas\_transform**
`🔗<class_Viewport_property_canvas_transform>`

classref-property-setget

-   `void (No return value.)` **set\_canvas\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_canvas\_transform**()

The canvas transform of the viewport, useful for changing the on-screen
positions of all child `CanvasItem<class_CanvasItem>`s. This is relative
to the global canvas transform of the viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DebugDraw<enum_Viewport_DebugDraw>` **debug\_draw** = `0`
`🔗<class_Viewport_property_debug_draw>`

classref-property-setget

-   `void (No return value.)` **set\_debug\_draw**(value:
    `DebugDraw<enum_Viewport_DebugDraw>`)
-   `DebugDraw<enum_Viewport_DebugDraw>` **get\_debug\_draw**()

The overlay mode for test rendered geometry in debug purposes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disable\_3d** = `false`
`🔗<class_Viewport_property_disable_3d>`

classref-property-setget

-   `void (No return value.)` **set\_disable\_3d**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_3d\_disabled**()

Disable 3D rendering (but keep 2D rendering).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fsr\_sharpness** = `0.2`
`🔗<class_Viewport_property_fsr_sharpness>`

classref-property-setget

-   `void (No return value.)` **set\_fsr\_sharpness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fsr\_sharpness**()

Determines how sharp the upscaled image will be when using the FSR
upscaling mode. Sharpness halves with every whole number. Values go from
0.0 (sharpest) to 2.0. Values above 2.0 won't make a visible difference.

To control this property on the root viewport, set the
`ProjectSettings.rendering/scaling_3d/fsr_sharpness<class_ProjectSettings_property_rendering/scaling_3d/fsr_sharpness>`
project setting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **global\_canvas\_transform**
`🔗<class_Viewport_property_global_canvas_transform>`

classref-property-setget

-   `void (No return value.)` **set\_global\_canvas\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>`
    **get\_global\_canvas\_transform**()

The global canvas transform of the viewport. The canvas transform is
relative to this.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gui\_disable\_input** = `false`
`🔗<class_Viewport_property_gui_disable_input>`

classref-property-setget

-   `void (No return value.)` **set\_disable\_input**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_input\_disabled**()

If `true`, the viewport will not receive input events.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gui\_embed\_subwindows** = `false`
`🔗<class_Viewport_property_gui_embed_subwindows>`

classref-property-setget

-   `void (No return value.)` **set\_embedding\_subwindows**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_embedding\_subwindows**()

If `true`, sub-windows (popups and dialogs) will be embedded inside
application window as control-like nodes. If `false`, they will appear
as separate windows handled by the operating system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gui\_snap\_controls\_to\_pixels** = `true`
`🔗<class_Viewport_property_gui_snap_controls_to_pixels>`

classref-property-setget

-   `void (No return value.)` **set\_snap\_controls\_to\_pixels**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_snap\_controls\_to\_pixels\_enabled**()

If `true`, the GUI controls on the viewport will lay pixel perfectly.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **handle\_input\_locally** = `true`
`🔗<class_Viewport_property_handle_input_locally>`

classref-property-setget

-   `void (No return value.)` **set\_handle\_input\_locally**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_handling\_input\_locally**()

If `true`, this viewport will mark incoming input events as handled by
itself. If `false`, this is instead done by the first parent viewport
that is set to handle input locally.

A `SubViewportContainer<class_SubViewportContainer>` will automatically
set this property to `false` for the **Viewport** contained inside of
it.

See also
`set_input_as_handled<class_Viewport_method_set_input_as_handled>` and
`is_input_handled<class_Viewport_method_is_input_handled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **mesh\_lod\_threshold** = `1.0`
`🔗<class_Viewport_property_mesh_lod_threshold>`

classref-property-setget

-   `void (No return value.)` **set\_mesh\_lod\_threshold**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_mesh\_lod\_threshold**()

The automatic LOD bias to use for meshes rendered within the
**Viewport** (this is analogous to
`ReflectionProbe.mesh_lod_threshold<class_ReflectionProbe_property_mesh_lod_threshold>`).
Higher values will use less detailed versions of meshes that have LOD
variations generated. If set to `0.0`, automatic LOD is disabled.
Increase
`mesh_lod_threshold<class_Viewport_property_mesh_lod_threshold>` to
improve performance at the cost of geometry detail.

To control this property on the root viewport, set the
`ProjectSettings.rendering/mesh_lod/lod_change/threshold_pixels<class_ProjectSettings_property_rendering/mesh_lod/lod_change/threshold_pixels>`
project setting.

\*\*Note:\*\*
`mesh_lod_threshold<class_Viewport_property_mesh_lod_threshold>` does
not affect `GeometryInstance3D<class_GeometryInstance3D>` visibility
ranges (also known as "manual" LOD or hierarchical LOD).

classref-item-separator

------------------------------------------------------------------------

classref-property

`MSAA<enum_Viewport_MSAA>` **msaa\_2d** = `0`
`🔗<class_Viewport_property_msaa_2d>`

classref-property-setget

-   `void (No return value.)` **set\_msaa\_2d**(value:
    `MSAA<enum_Viewport_MSAA>`)
-   `MSAA<enum_Viewport_MSAA>` **get\_msaa\_2d**()

The multisample anti-aliasing mode for 2D/Canvas rendering. A higher
number results in smoother edges at the cost of significantly worse
performance. A value of 2 or 4 is best unless targeting very high-end
systems. This has no effect on shader-induced aliasing or texture
aliasing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MSAA<enum_Viewport_MSAA>` **msaa\_3d** = `0`
`🔗<class_Viewport_property_msaa_3d>`

classref-property-setget

-   `void (No return value.)` **set\_msaa\_3d**(value:
    `MSAA<enum_Viewport_MSAA>`)
-   `MSAA<enum_Viewport_MSAA>` **get\_msaa\_3d**()

The multisample anti-aliasing mode for 3D rendering. A higher number
results in smoother edges at the cost of significantly worse
performance. A value of 2 or 4 is best unless targeting very high-end
systems. See also bilinear scaling 3d
`scaling_3d_mode<class_Viewport_property_scaling_3d_mode>` for
supersampling, which provides higher quality but is much more expensive.
This has no effect on shader-induced aliasing or texture aliasing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **own\_world\_3d** = `false`
`🔗<class_Viewport_property_own_world_3d>`

classref-property-setget

-   `void (No return value.)` **set\_use\_own\_world\_3d**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_own\_world\_3d**()

If `true`, the viewport will use a unique copy of the
`World3D<class_World3D>` defined in
`world_3d<class_Viewport_property_world_3d>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **physics\_object\_picking** = `false`
`🔗<class_Viewport_property_physics_object_picking>`

classref-property-setget

-   `void (No return value.)` **set\_physics\_object\_picking**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_physics\_object\_picking**()

If `true`, the objects rendered by viewport become subjects of mouse
picking process.

\*\*Note:\*\* The number of simultaneously pickable objects is limited
to 64 and they are selected in a non-deterministic order, which can be
different in each picking process.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **physics\_object\_picking\_first\_only** = `false`
`🔗<class_Viewport_property_physics_object_picking_first_only>`

classref-property-setget

-   `void (No return value.)`
    **set\_physics\_object\_picking\_first\_only**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_physics\_object\_picking\_first\_only**()

If `true`, the input\_event signal will only be sent to one physics
object in the mouse picking process. If you want to get the top object
only, you must also enable
`physics_object_picking_sort<class_Viewport_property_physics_object_picking_sort>`.

If `false`, an input\_event signal will be sent to all physics objects
in the mouse picking process.

This applies to 2D CanvasItem object picking only.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **physics\_object\_picking\_sort** = `false`
`🔗<class_Viewport_property_physics_object_picking_sort>`

classref-property-setget

-   `void (No return value.)`
    **set\_physics\_object\_picking\_sort**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_physics\_object\_picking\_sort**()

If `true`, objects receive mouse picking events sorted primarily by
their `CanvasItem.z_index<class_CanvasItem_property_z_index>` and
secondarily by their position in the scene tree. If `false`, the order
is undetermined.

\*\*Note:\*\* This setting is disabled by default because of its
potential expensive computational cost.

\*\*Note:\*\* Sorting happens after selecting the pickable objects.
Because of the limitation of 64 simultaneously pickable objects, it is
not guaranteed that the object with the highest
`CanvasItem.z_index<class_CanvasItem_property_z_index>` receives the
picking event.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **positional\_shadow\_atlas\_16\_bits** = `true`
`🔗<class_Viewport_property_positional_shadow_atlas_16_bits>`

classref-property-setget

-   `void (No return value.)`
    **set\_positional\_shadow\_atlas\_16\_bits**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_positional\_shadow\_atlas\_16\_bits**()

Use 16 bits for the omni/spot shadow depth map. Enabling this results in
shadows having less precision and may result in shadow acne, but can
lead to performance improvements on some devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**positional\_shadow\_atlas\_quad\_0** = `2`
`🔗<class_Viewport_property_positional_shadow_atlas_quad_0>`

classref-property-setget

-   `void (No return value.)`
    **set\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
    `int<class_int>`, subdiv:
    `PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`)
-   `PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
    **get\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The subdivision amount of the first quadrant on the shadow atlas.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**positional\_shadow\_atlas\_quad\_1** = `2`
`🔗<class_Viewport_property_positional_shadow_atlas_quad_1>`

classref-property-setget

-   `void (No return value.)`
    **set\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
    `int<class_int>`, subdiv:
    `PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`)
-   `PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
    **get\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The subdivision amount of the second quadrant on the shadow atlas.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**positional\_shadow\_atlas\_quad\_2** = `3`
`🔗<class_Viewport_property_positional_shadow_atlas_quad_2>`

classref-property-setget

-   `void (No return value.)`
    **set\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
    `int<class_int>`, subdiv:
    `PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`)
-   `PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
    **get\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The subdivision amount of the third quadrant on the shadow atlas.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**positional\_shadow\_atlas\_quad\_3** = `4`
`🔗<class_Viewport_property_positional_shadow_atlas_quad_3>`

classref-property-setget

-   `void (No return value.)`
    **set\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
    `int<class_int>`, subdiv:
    `PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`)
-   `PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
    **get\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The subdivision amount of the fourth quadrant on the shadow atlas.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **positional\_shadow\_atlas\_size** = `2048`
`🔗<class_Viewport_property_positional_shadow_atlas_size>`

classref-property-setget

-   `void (No return value.)`
    **set\_positional\_shadow\_atlas\_size**(value: `int<class_int>`)
-   `int<class_int>` **get\_positional\_shadow\_atlas\_size**()

The shadow atlas' resolution (used for omni and spot lights). The value
is rounded up to the nearest power of 2.

\*\*Note:\*\* If this is set to `0`, no positional shadows will be
visible at all. This can improve performance significantly on low-end
systems by reducing both the CPU and GPU load (as fewer draw calls are
needed to draw the scene without shadows).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Scaling3DMode<enum_Viewport_Scaling3DMode>` **scaling\_3d\_mode** = `0`
`🔗<class_Viewport_property_scaling_3d_mode>`

classref-property-setget

-   `void (No return value.)` **set\_scaling\_3d\_mode**(value:
    `Scaling3DMode<enum_Viewport_Scaling3DMode>`)
-   `Scaling3DMode<enum_Viewport_Scaling3DMode>`
    **get\_scaling\_3d\_mode**()

Sets scaling 3d mode. Bilinear scaling renders at different resolution
to either undersample or supersample the viewport. FidelityFX Super
Resolution 1.0, abbreviated to FSR, is an upscaling technology that
produces high quality images at fast framerates by using a spatially
aware upscaling algorithm. FSR is slightly more expensive than bilinear,
but it produces significantly higher image quality. FSR should be used
where possible.

To control this property on the root viewport, set the
`ProjectSettings.rendering/scaling_3d/mode<class_ProjectSettings_property_rendering/scaling_3d/mode>`
project setting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scaling\_3d\_scale** = `1.0`
`🔗<class_Viewport_property_scaling_3d_scale>`

classref-property-setget

-   `void (No return value.)` **set\_scaling\_3d\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_scaling\_3d\_scale**()

Scales the 3D render buffer based on the viewport size uses an image
filter specified in
`ProjectSettings.rendering/scaling_3d/mode<class_ProjectSettings_property_rendering/scaling_3d/mode>`
to scale the output image to the full viewport size. Values lower than
`1.0` can be used to speed up 3D rendering at the cost of quality
(undersampling). Values greater than `1.0` are only valid for bilinear
mode and can be used to improve 3D rendering quality at a high
performance cost (supersampling). See also
`ProjectSettings.rendering/anti_aliasing/quality/msaa_3d<class_ProjectSettings_property_rendering/anti_aliasing/quality/msaa_3d>`
for multi-sample antialiasing, which is significantly cheaper but only
smooths the edges of polygons.

When using FSR upscaling, AMD recommends exposing the following values
as preset options to users "Ultra Quality: 0.77", "Quality: 0.67",
"Balanced: 0.59", "Performance: 0.5" instead of exposing the entire
scale.

To control this property on the root viewport, set the
`ProjectSettings.rendering/scaling_3d/scale<class_ProjectSettings_property_rendering/scaling_3d/scale>`
project setting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ScreenSpaceAA<enum_Viewport_ScreenSpaceAA>` **screen\_space\_aa** = `0`
`🔗<class_Viewport_property_screen_space_aa>`

classref-property-setget

-   `void (No return value.)` **set\_screen\_space\_aa**(value:
    `ScreenSpaceAA<enum_Viewport_ScreenSpaceAA>`)
-   `ScreenSpaceAA<enum_Viewport_ScreenSpaceAA>`
    **get\_screen\_space\_aa**()

Sets the screen-space antialiasing method used. Screen-space
antialiasing works by selectively blurring edges in a post-process
shader. It differs from MSAA which takes multiple coverage samples while
rendering objects. Screen-space AA methods are typically faster than
MSAA and will smooth out specular aliasing, but tend to make scenes
appear blurry.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SDFOversize<enum_Viewport_SDFOversize>` **sdf\_oversize** = `1`
`🔗<class_Viewport_property_sdf_oversize>`

classref-property-setget

-   `void (No return value.)` **set\_sdf\_oversize**(value:
    `SDFOversize<enum_Viewport_SDFOversize>`)
-   `SDFOversize<enum_Viewport_SDFOversize>` **get\_sdf\_oversize**()

Controls how much of the original viewport's size should be covered by
the 2D signed distance field. This SDF can be sampled in
`CanvasItem<class_CanvasItem>` shaders and is also used for
`GPUParticles2D<class_GPUParticles2D>` collision. Higher values allow
portions of occluders located outside the viewport to still be taken
into account in the generated signed distance field, at the cost of
performance. If you notice particles falling through
`LightOccluder2D<class_LightOccluder2D>`s as the occluders leave the
viewport, increase this setting.

The percentage is added on each axis and on both sides. For example,
with the default
`SDF_OVERSIZE_120_PERCENT<class_Viewport_constant_SDF_OVERSIZE_120_PERCENT>`,
the signed distance field will cover 20% of the viewport's size outside
the viewport on each side (top, right, bottom, left).

classref-item-separator

------------------------------------------------------------------------

classref-property

`SDFScale<enum_Viewport_SDFScale>` **sdf\_scale** = `1`
`🔗<class_Viewport_property_sdf_scale>`

classref-property-setget

-   `void (No return value.)` **set\_sdf\_scale**(value:
    `SDFScale<enum_Viewport_SDFScale>`)
-   `SDFScale<enum_Viewport_SDFScale>` **get\_sdf\_scale**()

The resolution scale to use for the 2D signed distance field. Higher
values lead to a more precise and more stable signed distance field as
the camera moves, at the cost of performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **snap\_2d\_transforms\_to\_pixel** = `false`
`🔗<class_Viewport_property_snap_2d_transforms_to_pixel>`

classref-property-setget

-   `void (No return value.)`
    **set\_snap\_2d\_transforms\_to\_pixel**(value: `bool<class_bool>`)
-   `bool<class_bool>`
    **is\_snap\_2d\_transforms\_to\_pixel\_enabled**()

If `true`, `CanvasItem<class_CanvasItem>` nodes will internally snap to
full pixels. Their position can still be sub-pixel, but the decimals
will not have effect. This can lead to a crisper appearance at the cost
of less smooth movement, especially when `Camera2D<class_Camera2D>`
smoothing is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **snap\_2d\_vertices\_to\_pixel** = `false`
`🔗<class_Viewport_property_snap_2d_vertices_to_pixel>`

classref-property-setget

-   `void (No return value.)`
    **set\_snap\_2d\_vertices\_to\_pixel**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_snap\_2d\_vertices\_to\_pixel\_enabled**()

If `true`, vertices of `CanvasItem<class_CanvasItem>` nodes will snap to
full pixels. Only affects the final vertex positions, not the
transforms. This can lead to a crisper appearance at the cost of less
smooth movement, especially when `Camera2D<class_Camera2D>` smoothing is
enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **texture\_mipmap\_bias** = `0.0`
`🔗<class_Viewport_property_texture_mipmap_bias>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_mipmap\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_texture\_mipmap\_bias**()

Affects the final texture sharpness by reading from a lower or higher
mipmap (also called "texture LOD bias"). Negative values make mipmapped
textures sharper but grainier when viewed at a distance, while positive
values make mipmapped textures blurrier (even when up close).

Enabling temporal antialiasing
(`use_taa<class_Viewport_property_use_taa>`) will automatically apply a
`-0.5` offset to this value, while enabling FXAA
(`screen_space_aa<class_Viewport_property_screen_space_aa>`) will
automatically apply a `-0.25` offset to this value. If both TAA and FXAA
are enabled at the same time, an offset of `-0.75` is applied to this
value.

\*\*Note:\*\* If
`scaling_3d_scale<class_Viewport_property_scaling_3d_scale>` is lower
than `1.0` (exclusive),
`texture_mipmap_bias<class_Viewport_property_texture_mipmap_bias>` is
used to adjust the automatic mipmap bias which is calculated internally
based on the scale factor. The formula for this is
`log2(scaling_3d_scale) + mipmap_bias`.

To control this property on the root viewport, set the
`ProjectSettings.rendering/textures/default_filters/texture_mipmap_bias<class_ProjectSettings_property_rendering/textures/default_filters/texture_mipmap_bias>`
project setting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **transparent\_bg** = `false`
`🔗<class_Viewport_property_transparent_bg>`

classref-property-setget

-   `void (No return value.)` **set\_transparent\_background**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **has\_transparent\_background**()

If `true`, the viewport should render its background as transparent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_debanding** = `false`
`🔗<class_Viewport_property_use_debanding>`

classref-property-setget

-   `void (No return value.)` **set\_use\_debanding**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_debanding**()

If `true`, uses a fast post-processing filter to make banding
significantly less visible in 3D. 2D rendering is *not* affected by
debanding unless the
`Environment.background_mode<class_Environment_property_background_mode>`
is `Environment.BG_CANVAS<class_Environment_constant_BG_CANVAS>`. See
also
`ProjectSettings.rendering/anti_aliasing/quality/use_debanding<class_ProjectSettings_property_rendering/anti_aliasing/quality/use_debanding>`.

In some cases, debanding may introduce a slightly noticeable dithering
pattern. It's recommended to enable debanding only when actually needed
since the dithering pattern will make lossless-compressed screenshots
larger.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_hdr\_2d** = `false`
`🔗<class_Viewport_property_use_hdr_2d>`

classref-property-setget

-   `void (No return value.)` **set\_use\_hdr\_2d**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_hdr\_2d**()

If `true`, 2D rendering will use an high dynamic range (HDR) format
framebuffer matching the bit depth of the 3D framebuffer. When using the
Forward+ renderer this will be an `RGBA16` framebuffer, while when using
the Mobile renderer it will be an `RGB10_A2` framebuffer. Additionally,
2D rendering will take place in linear color space and will be converted
to sRGB space immediately before blitting to the screen (if the Viewport
is attached to the screen). Practically speaking, this means that the
end result of the Viewport will not be clamped into the `0-1` range and
can be used in 3D rendering without color space adjustments. This allows
2D rendering to take advantage of effects requiring high dynamic range
(e.g. 2D glow) as well as substantially improves the appearance of
effects requiring highly detailed gradients.

\*\*Note:\*\* This setting will have no effect when using the GL
Compatibility renderer as the GL Compatibility renderer always renders
in low dynamic range for performance reasons.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_occlusion\_culling** = `false`
`🔗<class_Viewport_property_use_occlusion_culling>`

classref-property-setget

-   `void (No return value.)` **set\_use\_occlusion\_culling**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_occlusion\_culling**()

If `true`, `OccluderInstance3D<class_OccluderInstance3D>` nodes will be
usable for occlusion culling in 3D for this viewport. For the root
viewport,
`ProjectSettings.rendering/occlusion_culling/use_occlusion_culling<class_ProjectSettings_property_rendering/occlusion_culling/use_occlusion_culling>`
must be set to `true` instead.

\*\*Note:\*\* Enabling occlusion culling has a cost on the CPU. Only
enable occlusion culling if you actually plan to use it, and think
whether your scene can actually benefit from occlusion culling. Large,
open scenes with few or no objects blocking the view will generally not
benefit much from occlusion culling. Large open scenes generally benefit
more from mesh LOD and visibility ranges
(`GeometryInstance3D.visibility_range_begin<class_GeometryInstance3D_property_visibility_range_begin>`
and
`GeometryInstance3D.visibility_range_end<class_GeometryInstance3D_property_visibility_range_end>`)
compared to occlusion culling.

\*\*Note:\*\* Due to memory constraints, occlusion culling is not
supported by default in Web export templates. It can be enabled by
compiling custom Web export templates with `module_raycast_enabled=yes`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_taa** = `false`
`🔗<class_Viewport_property_use_taa>`

classref-property-setget

-   `void (No return value.)` **set\_use\_taa**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_taa**()

Enables Temporal Anti-Aliasing for this viewport. TAA works by jittering
the camera and accumulating the images of the last rendered frames,
motion vector rendering is used to account for camera and object motion.

\*\*Note:\*\* The implementation is not complete yet, some visual
instances such as particles and skinned meshes may show artifacts.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_xr** = `false`
`🔗<class_Viewport_property_use_xr>`

classref-property-setget

-   `void (No return value.)` **set\_use\_xr**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_xr**()

If `true`, the viewport will use the primary XR interface to render XR
output. When applicable this can result in a stereoscopic image and the
resulting render being output to a headset.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VRSMode<enum_Viewport_VRSMode>` **vrs\_mode** = `0`
`🔗<class_Viewport_property_vrs_mode>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_mode**(value:
    `VRSMode<enum_Viewport_VRSMode>`)
-   `VRSMode<enum_Viewport_VRSMode>` **get\_vrs\_mode**()

The Variable Rate Shading (VRS) mode that is used for this viewport.
Note, if hardware does not support VRS this property is ignored.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **vrs\_texture**
`🔗<class_Viewport_property_vrs_texture>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_vrs\_texture**()

Texture to use when `vrs_mode<class_Viewport_property_vrs_mode>` is set
to `VRS_TEXTURE<class_Viewport_constant_VRS_TEXTURE>`.

The texture *must* use a lossless compression format so that colors can
be matched precisely. The following VRS densities are mapped to various
colors, with brighter colors representing a lower level of shading
precision:

    - 1×1 = rgb(0, 0, 0)     - #000000
    - 1×2 = rgb(0, 85, 0)    - #005500
    - 2×1 = rgb(85, 0, 0)    - #550000
    - 2×2 = rgb(85, 85, 0)   - #555500
    - 2×4 = rgb(85, 170, 0)  - #55aa00
    - 4×2 = rgb(170, 85, 0)  - #aa5500
    - 4×4 = rgb(170, 170, 0) - #aaaa00
    - 4×8 = rgb(170, 255, 0) - #aaff00 - Not supported on most hardware
    - 8×4 = rgb(255, 170, 0) - #ffaa00 - Not supported on most hardware
    - 8×8 = rgb(255, 255, 0) - #ffff00 - Not supported on most hardware

classref-item-separator

------------------------------------------------------------------------

classref-property

`VRSUpdateMode<enum_Viewport_VRSUpdateMode>` **vrs\_update\_mode** = `1`
`🔗<class_Viewport_property_vrs_update_mode>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_update\_mode**(value:
    `VRSUpdateMode<enum_Viewport_VRSUpdateMode>`)
-   `VRSUpdateMode<enum_Viewport_VRSUpdateMode>`
    **get\_vrs\_update\_mode**()

Sets the update mode for Variable Rate Shading (VRS) for the viewport.
VRS requires the input texture to be converted to the format usable by
the VRS method supported by the hardware. The update mode defines how
often this happens. If the GPU does not support VRS, or VRS is not
enabled, this property is ignored.

classref-item-separator

------------------------------------------------------------------------

classref-property

`World2D<class_World2D>` **world\_2d**
`🔗<class_Viewport_property_world_2d>`

classref-property-setget

-   `void (No return value.)` **set\_world\_2d**(value:
    `World2D<class_World2D>`)
-   `World2D<class_World2D>` **get\_world\_2d**()

The custom `World2D<class_World2D>` which can be used as 2D environment
source.

classref-item-separator

------------------------------------------------------------------------

classref-property

`World3D<class_World3D>` **world\_3d**
`🔗<class_Viewport_property_world_3d>`

classref-property-setget

-   `void (No return value.)` **set\_world\_3d**(value:
    `World3D<class_World3D>`)
-   `World3D<class_World3D>` **get\_world\_3d**()

The custom `World3D<class_World3D>` which can be used as 3D environment
source.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`World2D<class_World2D>` **find\_world\_2d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_find_world_2d>`

Returns the first valid `World2D<class_World2D>` for this viewport,
searching the `world_2d<class_Viewport_property_world_2d>` property of
itself and any Viewport ancestor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`World3D<class_World3D>` **find\_world\_3d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_find_world_3d>`

Returns the first valid `World3D<class_World3D>` for this viewport,
searching the `world_3d<class_Viewport_property_world_3d>` property of
itself and any Viewport ancestor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioListener2D<class_AudioListener2D>` **get\_audio\_listener\_2d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_audio_listener_2d>`

Returns the currently active 2D audio listener. Returns `null` if there
are no active 2D audio listeners, in which case the active 2D camera
will be treated as listener.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioListener3D<class_AudioListener3D>` **get\_audio\_listener\_3d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_audio_listener_3d>`

Returns the currently active 3D audio listener. Returns `null` if there
are no active 3D audio listeners, in which case the active 3D camera
will be treated as listener.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Camera2D<class_Camera2D>` **get\_camera\_2d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_camera_2d>`

Returns the currently active 2D camera. Returns null if there are no
active cameras.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Camera3D<class_Camera3D>` **get\_camera\_3d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_camera_3d>`

Returns the currently active 3D camera.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_canvas\_cull\_mask\_bit**(layer:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_canvas_cull_mask_bit>`

Returns an individual bit on the rendering layer mask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Window<class_Window>`\]
**get\_embedded\_subwindows**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_embedded_subwindows>`

Returns a list of the visible embedded `Window<class_Window>`s inside
the viewport.

\*\*Note:\*\* `Window<class_Window>`s inside other viewports will not be
listed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **get\_final\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_final_transform>`

Returns the transform from the viewport's coordinate system to the
embedder's coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_mouse\_position**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_mouse_position>`

Returns the mouse's position in this **Viewport** using the coordinate
system of this **Viewport**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`
**get\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_positional_shadow_atlas_quadrant_subdiv>`

Returns the positional shadow atlas quadrant subdivision of the
specified quadrant.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_render\_info**(type:
`RenderInfoType<enum_Viewport_RenderInfoType>`, info:
`RenderInfo<enum_Viewport_RenderInfo>`)
`🔗<class_Viewport_method_get_render_info>`

Returns rendering statistics of the given type. See
`RenderInfoType<enum_Viewport_RenderInfoType>` and
`RenderInfo<enum_Viewport_RenderInfo>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **get\_screen\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_screen_transform>`

Returns the transform from the Viewport's coordinates to the screen
coordinates of the containing window manager window.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ViewportTexture<class_ViewportTexture>` **get\_texture**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_texture>`

Returns the viewport's texture.

\*\*Note:\*\* When trying to store the current texture (e.g. in a file),
it might be completely black or outdated if used too early, especially
when used in e.g. `Node._ready<class_Node_private_method__ready>`. To
make sure the texture you get is correct, you can await
`RenderingServer.frame_post_draw<class_RenderingServer_signal_frame_post_draw>`
signal.

    func _ready():
        await RenderingServer.frame_post_draw
        $Viewport.get_texture().get_image().save_png("user://Screenshot.png")

\*\*Note:\*\* When `use_hdr_2d<class_Viewport_property_use_hdr_2d>` is
`true` the returned texture will be an HDR image encoded in linear
space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_viewport\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_viewport_rid>`

Returns the viewport's RID from the
`RenderingServer<class_RenderingServer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_visible\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_get_visible_rect>`

Returns the visible rectangle in global screen coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **gui\_cancel\_drag**()
`🔗<class_Viewport_method_gui_cancel_drag>`

Cancels the drag operation that was previously started through
`Control._get_drag_data<class_Control_private_method__get_drag_data>` or
forced with `Control.force_drag<class_Control_method_force_drag>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **gui\_get\_drag\_data**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_gui_get_drag_data>`

Returns the drag data from the GUI, that was previously returned by
`Control._get_drag_data<class_Control_private_method__get_drag_data>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **gui\_get\_focus\_owner**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_gui_get_focus_owner>`

Returns the `Control<class_Control>` having the focus within this
viewport. If no `Control<class_Control>` has the focus, returns null.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **gui\_get\_hovered\_control**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_gui_get_hovered_control>`

Returns the `Control<class_Control>` that the mouse is currently
hovering over in this viewport. If no `Control<class_Control>` has the
cursor, returns null.

Typically the leaf `Control<class_Control>` node or deepest level of the
subtree which claims hover. This is very useful when used together with
`Node.is_ancestor_of<class_Node_method_is_ancestor_of>` to find if the
mouse is within a control tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **gui\_is\_drag\_successful**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_gui_is_drag_successful>`

Returns `true` if the drag operation is successful.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **gui\_is\_dragging**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_gui_is_dragging>`

Returns `true` if a drag operation is currently ongoing and where the
drop action could happen in this viewport.

Alternative to
`Node.NOTIFICATION_DRAG_BEGIN<class_Node_constant_NOTIFICATION_DRAG_BEGIN>`
and
`Node.NOTIFICATION_DRAG_END<class_Node_constant_NOTIFICATION_DRAG_END>`
when you prefer polling the value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **gui\_release\_focus**()
`🔗<class_Viewport_method_gui_release_focus>`

Removes the focus from the currently focused `Control<class_Control>`
within this viewport. If no `Control<class_Control>` has the focus, does
nothing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_input\_handled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Viewport_method_is_input_handled>`

Returns whether the current `InputEvent<class_InputEvent>` has been
handled. Input events are not handled until
`set_input_as_handled<class_Viewport_method_set_input_as_handled>` has
been called during the lifetime of an `InputEvent<class_InputEvent>`.

This is usually done as part of input handling methods like
`Node._input<class_Node_private_method__input>`,
`Control._gui_input<class_Control_private_method__gui_input>` or others,
as well as in corresponding signal handlers.

If `handle_input_locally<class_Viewport_property_handle_input_locally>`
is set to `false`, this method will try finding the first parent
viewport that is set to handle input locally, and return its value for
`is_input_handled<class_Viewport_method_is_input_handled>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_input**(event:
`InputEvent<class_InputEvent>`, in\_local\_coords: `bool<class_bool>` =
false) `🔗<class_Viewport_method_push_input>`

Triggers the given `event` in this **Viewport**. This can be used to
pass an `InputEvent<class_InputEvent>` between viewports, or to locally
apply inputs that were sent over the network or saved to a file.

If `in_local_coords` is `false`, the event's position is in the
embedder's coordinates and will be converted to viewport coordinates. If
`in_local_coords` is `true`, the event's position is in viewport
coordinates.

While this method serves a similar purpose as
`Input.parse_input_event<class_Input_method_parse_input_event>`, it does
not remap the specified `event` based on project settings like
`ProjectSettings.input_devices/pointing/emulate_touch_from_mouse<class_ProjectSettings_property_input_devices/pointing/emulate_touch_from_mouse>`.

Calling this method will propagate calls to child nodes for following
methods in the given order:

-   `Node._input<class_Node_private_method__input>`
-   `Control._gui_input<class_Control_private_method__gui_input>` for
    `Control<class_Control>` nodes
-   `Node._shortcut_input<class_Node_private_method__shortcut_input>`
-   `Node._unhandled_key_input<class_Node_private_method__unhandled_key_input>`
-   `Node._unhandled_input<class_Node_private_method__unhandled_input>`

If an earlier method marks the input as handled via
`set_input_as_handled<class_Viewport_method_set_input_as_handled>`, any
later method in this list will not be called.

If none of the methods handle the event and
`physics_object_picking<class_Viewport_property_physics_object_picking>`
is `true`, the event is used for physics object picking.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_text\_input**(text:
`String<class_String>`) `🔗<class_Viewport_method_push_text_input>`

Helper method which calls the `set_text()` method on the currently
focused `Control<class_Control>`, provided that it is defined (e.g. if
the focused Control is `Button<class_Button>` or
`LineEdit<class_LineEdit>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_unhandled\_input**(event:
`InputEvent<class_InputEvent>`, in\_local\_coords: `bool<class_bool>` =
false) `🔗<class_Viewport_method_push_unhandled_input>`

**Deprecated:** Use `push_input<class_Viewport_method_push_input>`
instead.

Triggers the given `event` in this **Viewport**. This can be used to
pass an `InputEvent<class_InputEvent>` between viewports, or to locally
apply inputs that were sent over the network or saved to a file.

If `in_local_coords` is `false`, the event's position is in the
embedder's coordinates and will be converted to viewport coordinates. If
`in_local_coords` is `true`, the event's position is in viewport
coordinates.

Calling this method will propagate calls to child nodes for following
methods in the given order:

-   `Node._shortcut_input<class_Node_private_method__shortcut_input>`
-   `Node._unhandled_key_input<class_Node_private_method__unhandled_key_input>`
-   `Node._unhandled_input<class_Node_private_method__unhandled_input>`

If an earlier method marks the input as handled via
`set_input_as_handled<class_Viewport_method_set_input_as_handled>`, any
later method in this list will not be called.

If none of the methods handle the event and
`physics_object_picking<class_Viewport_property_physics_object_picking>`
is `true`, the event is used for physics object picking.

\*\*Note:\*\* This method doesn't propagate input events to embedded
`Window<class_Window>`s or `SubViewport<class_SubViewport>`s.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_canvas\_cull\_mask\_bit**(layer:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_Viewport_method_set_canvas_cull_mask_bit>`

Set/clear individual bits on the rendering layer mask. This simplifies
editing this **Viewport**'s layers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_input\_as\_handled**()
`🔗<class_Viewport_method_set_input_as_handled>`

Stops the input from propagating further down the
`SceneTree<class_SceneTree>`.

\*\*Note:\*\* This does not affect the methods in `Input<class_Input>`,
only the way events are propagated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_positional\_shadow\_atlas\_quadrant\_subdiv**(quadrant:
`int<class_int>`, subdiv:
`PositionalShadowAtlasQuadrantSubdiv<enum_Viewport_PositionalShadowAtlasQuadrantSubdiv>`)
`🔗<class_Viewport_method_set_positional_shadow_atlas_quadrant_subdiv>`

Sets the number of subdivisions to use in the specified quadrant. A
higher number of subdivisions allows you to have more shadows in the
scene at once, but reduces the quality of the shadows. A good practice
is to have quadrants with a varying number of subdivisions and to have
as few subdivisions as possible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_mouse\_cursor\_state**()
`🔗<class_Viewport_method_update_mouse_cursor_state>`

Force instantly updating the display based on the current mouse cursor
position. This includes updating the mouse cursor shape and sending
necessary `Control.mouse_entered<class_Control_signal_mouse_entered>`,
`CollisionObject2D.mouse_entered<class_CollisionObject2D_signal_mouse_entered>`,
`CollisionObject3D.mouse_entered<class_CollisionObject3D_signal_mouse_entered>`
and `Window.mouse_entered<class_Window_signal_mouse_entered>` signals
and their respective `mouse_exited` counterparts.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **warp\_mouse**(position:
`Vector2<class_Vector2>`) `🔗<class_Viewport_method_warp_mouse>`

Moves the mouse pointer to the specified position in this **Viewport**
using the coordinate system of this **Viewport**.

\*\*Note:\*\* `warp_mouse<class_Viewport_method_warp_mouse>` is only
supported on Windows, macOS and Linux. It has no effect on Android, iOS
and Web.
