github\_url  
hide

# Image

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Image datatype.

classref-introduction-group

## Description

Native image datatype. Contains image data which can be converted to an
`ImageTexture<class_ImageTexture>` and provides commonly used *image
processing* methods. The maximum width and height for an **Image** are
`MAX_WIDTH<class_Image_constant_MAX_WIDTH>` and
`MAX_HEIGHT<class_Image_constant_MAX_HEIGHT>`.

An **Image** cannot be assigned to a texture property of an object
directly (such as `Sprite2D.texture<class_Sprite2D_property_texture>`),
and has to be converted manually to an
`ImageTexture<class_ImageTexture>` first.

\*\*Note:\*\* The maximum image size is 16384×16384 pixels due to
graphics hardware limitations. Larger images may fail to import.

classref-introduction-group

## Tutorials

-   `Importing images <../tutorials/assets_pipeline/importing_images>`
-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`

classref-reftable-group

## Properties

<table>
<tbody>
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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

enum **Format**: `🔗<enum_Image_Format>`

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_L8** = `0`

Texture format with a single 8-bit depth representing luminance.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_LA8** = `1`

OpenGL texture format with two values, luminance and alpha each stored
with 8 bits.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_R8** = `2`

OpenGL texture format `RED` with a single component and a bitdepth of 8.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RG8** = `3`

OpenGL texture format `RG` with two components and a bitdepth of 8 for
each.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGB8** = `4`

OpenGL texture format `RGB` with three components, each with a bitdepth
of 8.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGBA8** = `5`

OpenGL texture format `RGBA` with four components, each with a bitdepth
of 8.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGBA4444** = `6`

OpenGL texture format `RGBA` with four components, each with a bitdepth
of 4.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGB565** = `7`

OpenGL texture format `RGB` with three components. Red and blue have a
bitdepth of 5, and green has a bitdepth of 6.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RF** = `8`

OpenGL texture format `GL_R32F` where there's one component, a 32-bit
floating-point value.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGF** = `9`

OpenGL texture format `GL_RG32F` where there are two components, each a
32-bit floating-point values.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGBF** = `10`

OpenGL texture format `GL_RGB32F` where there are three components, each
a 32-bit floating-point values.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGBAF** = `11`

OpenGL texture format `GL_RGBA32F` where there are four components, each
a 32-bit floating-point values.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RH** = `12`

OpenGL texture format `GL_R16F` where there's one component, a 16-bit
"half-precision" floating-point value.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGH** = `13`

OpenGL texture format `GL_RG16F` where there are two components, each a
16-bit "half-precision" floating-point value.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGBH** = `14`

OpenGL texture format `GL_RGB16F` where there are three components, each
a 16-bit "half-precision" floating-point value.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGBAH** = `15`

OpenGL texture format `GL_RGBA16F` where there are four components, each
a 16-bit "half-precision" floating-point value.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGBE9995** = `16`

A special OpenGL texture format where the three color components have 9
bits of precision and all three share a single 5-bit exponent.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_DXT1** = `17`

The [S3TC](https://en.wikipedia.org/wiki/S3_Texture_Compression) texture
format that uses Block Compression 1, and is the smallest variation of
S3TC, only providing 1 bit of alpha and color data being premultiplied
with alpha.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_DXT3** = `18`

The [S3TC](https://en.wikipedia.org/wiki/S3_Texture_Compression) texture
format that uses Block Compression 2, and color data is interpreted as
not having been premultiplied by alpha. Well suited for images with
sharp alpha transitions between translucent and opaque areas.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_DXT5** = `19`

The [S3TC](https://en.wikipedia.org/wiki/S3_Texture_Compression) texture
format also known as Block Compression 3 or BC3 that contains 64 bits of
alpha channel data followed by 64 bits of DXT1-encoded color data. Color
data is not premultiplied by alpha, same as DXT3. DXT5 generally
produces superior results for transparent gradients compared to DXT3.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGTC\_R** = `20`

Texture format that uses [Red Green Texture
Compression](https://www.khronos.org/opengl/wiki/Red_Green_Texture_Compression),
normalizing the red channel data using the same compression algorithm
that DXT5 uses for the alpha channel.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_RGTC\_RG** = `21`

Texture format that uses [Red Green Texture
Compression](https://www.khronos.org/opengl/wiki/Red_Green_Texture_Compression),
normalizing the red and green channel data using the same compression
algorithm that DXT5 uses for the alpha channel.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_BPTC\_RGBA** = `22`

Texture format that uses
[BPTC](https://www.khronos.org/opengl/wiki/BPTC_Texture_Compression)
compression with unsigned normalized RGBA components.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_BPTC\_RGBF** = `23`

Texture format that uses
[BPTC](https://www.khronos.org/opengl/wiki/BPTC_Texture_Compression)
compression with signed floating-point RGB components.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_BPTC\_RGBFU** = `24`

Texture format that uses
[BPTC](https://www.khronos.org/opengl/wiki/BPTC_Texture_Compression)
compression with unsigned floating-point RGB components.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC** = `25`

[Ericsson Texture Compression format
1](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC1),
also referred to as "ETC1", and is part of the OpenGL ES graphics
standard. This format cannot store an alpha channel.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC2\_R11** = `26`

[Ericsson Texture Compression format
2](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC2_and_EAC)
(`R11_EAC` variant), which provides one channel of unsigned data.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC2\_R11S** = `27`

[Ericsson Texture Compression format
2](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC2_and_EAC)
(`SIGNED_R11_EAC` variant), which provides one channel of signed data.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC2\_RG11** = `28`

[Ericsson Texture Compression format
2](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC2_and_EAC)
(`RG11_EAC` variant), which provides two channels of unsigned data.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC2\_RG11S** = `29`

[Ericsson Texture Compression format
2](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC2_and_EAC)
(`SIGNED_RG11_EAC` variant), which provides two channels of signed data.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC2\_RGB8** = `30`

[Ericsson Texture Compression format
2](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC2_and_EAC)
(`RGB8` variant), which is a follow-up of ETC1 and compresses RGB888
data.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC2\_RGBA8** = `31`

[Ericsson Texture Compression format
2](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC2_and_EAC)
(`RGBA8`variant), which compresses RGBA8888 data with full alpha
support.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC2\_RGB8A1** = `32`

[Ericsson Texture Compression format
2](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC2_and_EAC)
(`RGB8_PUNCHTHROUGH_ALPHA1` variant), which compresses RGBA data to make
alpha either fully transparent or fully opaque.

\*\*Note:\*\* When creating an `ImageTexture<class_ImageTexture>`, an
sRGB to linear color space conversion is performed.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ETC2\_RA\_AS\_RG** = `33`

[Ericsson Texture Compression format
2](https://en.wikipedia.org/wiki/Ericsson_Texture_Compression#ETC2_and_EAC)
(`RGBA8` variant), which compresses RA data and interprets it as two
channels (red and green). See also
`FORMAT_ETC2_RGBA8<class_Image_constant_FORMAT_ETC2_RGBA8>`.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_DXT5\_RA\_AS\_RG** = `34`

The [S3TC](https://en.wikipedia.org/wiki/S3_Texture_Compression) texture
format also known as Block Compression 3 or BC3, which compresses RA
data and interprets it as two channels (red and green). See also
`FORMAT_DXT5<class_Image_constant_FORMAT_DXT5>`.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ASTC\_4x4** = `35`

[Adaptive Scalable Texture
Compression](https://en.wikipedia.org/wiki/Adaptive_scalable_texture_compression).
This implements the 4×4 (high quality) mode.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ASTC\_4x4\_HDR** = `36`

Same format as `FORMAT_ASTC_4x4<class_Image_constant_FORMAT_ASTC_4x4>`,
but with the hint to let the GPU know it is used for HDR.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ASTC\_8x8** = `37`

[Adaptive Scalable Texture
Compression](https://en.wikipedia.org/wiki/Adaptive_scalable_texture_compression).
This implements the 8×8 (low quality) mode.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_ASTC\_8x8\_HDR** = `38`

Same format as `FORMAT_ASTC_8x8<class_Image_constant_FORMAT_ASTC_8x8>`,
but with the hint to let the GPU know it is used for HDR.

classref-enumeration-constant

`Format<enum_Image_Format>` **FORMAT\_MAX** = `39`

Represents the size of the `Format<enum_Image_Format>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Interpolation**: `🔗<enum_Image_Interpolation>`

classref-enumeration-constant

`Interpolation<enum_Image_Interpolation>` **INTERPOLATE\_NEAREST** = `0`

Performs nearest-neighbor interpolation. If the image is resized, it
will be pixelated.

classref-enumeration-constant

`Interpolation<enum_Image_Interpolation>` **INTERPOLATE\_BILINEAR** =
`1`

Performs bilinear interpolation. If the image is resized, it will be
blurry. This mode is faster than
`INTERPOLATE_CUBIC<class_Image_constant_INTERPOLATE_CUBIC>`, but it
results in lower quality.

classref-enumeration-constant

`Interpolation<enum_Image_Interpolation>` **INTERPOLATE\_CUBIC** = `2`

Performs cubic interpolation. If the image is resized, it will be
blurry. This mode often gives better results compared to
`INTERPOLATE_BILINEAR<class_Image_constant_INTERPOLATE_BILINEAR>`, at
the cost of being slower.

classref-enumeration-constant

`Interpolation<enum_Image_Interpolation>` **INTERPOLATE\_TRILINEAR** =
`3`

Performs bilinear separately on the two most-suited mipmap levels, then
linearly interpolates between them.

It's slower than
`INTERPOLATE_BILINEAR<class_Image_constant_INTERPOLATE_BILINEAR>`, but
produces higher-quality results with far fewer aliasing artifacts.

If the image does not have mipmaps, they will be generated and used
internally, but no mipmaps will be generated on the resulting image.

\*\*Note:\*\* If you intend to scale multiple copies of the original
image, it's better to call
`generate_mipmaps<class_Image_method_generate_mipmaps>`\] on it in
advance, to avoid wasting processing power in generating them again and
again.

On the other hand, if the image already has mipmaps, they will be used,
and a new set will be generated for the resulting image.

classref-enumeration-constant

`Interpolation<enum_Image_Interpolation>` **INTERPOLATE\_LANCZOS** = `4`

Performs Lanczos interpolation. This is the slowest image resizing mode,
but it typically gives the best results, especially when downscaling
images.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AlphaMode**: `🔗<enum_Image_AlphaMode>`

classref-enumeration-constant

`AlphaMode<enum_Image_AlphaMode>` **ALPHA\_NONE** = `0`

Image does not have alpha.

classref-enumeration-constant

`AlphaMode<enum_Image_AlphaMode>` **ALPHA\_BIT** = `1`

Image stores alpha in a single bit.

classref-enumeration-constant

`AlphaMode<enum_Image_AlphaMode>` **ALPHA\_BLEND** = `2`

Image uses alpha.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CompressMode**: `🔗<enum_Image_CompressMode>`

classref-enumeration-constant

`CompressMode<enum_Image_CompressMode>` **COMPRESS\_S3TC** = `0`

Use S3TC compression.

classref-enumeration-constant

`CompressMode<enum_Image_CompressMode>` **COMPRESS\_ETC** = `1`

Use ETC compression.

classref-enumeration-constant

`CompressMode<enum_Image_CompressMode>` **COMPRESS\_ETC2** = `2`

Use ETC2 compression.

classref-enumeration-constant

`CompressMode<enum_Image_CompressMode>` **COMPRESS\_BPTC** = `3`

Use BPTC compression.

classref-enumeration-constant

`CompressMode<enum_Image_CompressMode>` **COMPRESS\_ASTC** = `4`

Use ASTC compression.

classref-enumeration-constant

`CompressMode<enum_Image_CompressMode>` **COMPRESS\_MAX** = `5`

Represents the size of the `CompressMode<enum_Image_CompressMode>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **UsedChannels**: `🔗<enum_Image_UsedChannels>`

classref-enumeration-constant

`UsedChannels<enum_Image_UsedChannels>` **USED\_CHANNELS\_L** = `0`

The image only uses one channel for luminance (grayscale).

classref-enumeration-constant

`UsedChannels<enum_Image_UsedChannels>` **USED\_CHANNELS\_LA** = `1`

The image uses two channels for luminance and alpha, respectively.

classref-enumeration-constant

`UsedChannels<enum_Image_UsedChannels>` **USED\_CHANNELS\_R** = `2`

The image only uses the red channel.

classref-enumeration-constant

`UsedChannels<enum_Image_UsedChannels>` **USED\_CHANNELS\_RG** = `3`

The image uses two channels for red and green.

classref-enumeration-constant

`UsedChannels<enum_Image_UsedChannels>` **USED\_CHANNELS\_RGB** = `4`

The image uses three channels for red, green, and blue.

classref-enumeration-constant

`UsedChannels<enum_Image_UsedChannels>` **USED\_CHANNELS\_RGBA** = `5`

The image uses four channels for red, green, blue, and alpha.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CompressSource**: `🔗<enum_Image_CompressSource>`

classref-enumeration-constant

`CompressSource<enum_Image_CompressSource>`
**COMPRESS\_SOURCE\_GENERIC** = `0`

Source texture (before compression) is a regular texture. Default for
all textures.

classref-enumeration-constant

`CompressSource<enum_Image_CompressSource>` **COMPRESS\_SOURCE\_SRGB** =
`1`

Source texture (before compression) is in sRGB space.

classref-enumeration-constant

`CompressSource<enum_Image_CompressSource>` **COMPRESS\_SOURCE\_NORMAL**
= `2`

Source texture (before compression) is a normal texture (e.g. it can be
compressed into two channels).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ASTCFormat**: `🔗<enum_Image_ASTCFormat>`

classref-enumeration-constant

`ASTCFormat<enum_Image_ASTCFormat>` **ASTC\_FORMAT\_4x4** = `0`

Hint to indicate that the high quality 4×4 ASTC compression format
should be used.

classref-enumeration-constant

`ASTCFormat<enum_Image_ASTCFormat>` **ASTC\_FORMAT\_8x8** = `1`

Hint to indicate that the low quality 8×8 ASTC compression format should
be used.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**MAX\_WIDTH** = `16777216` `🔗<class_Image_constant_MAX_WIDTH>`

The maximal width allowed for **Image** resources.

classref-constant

**MAX\_HEIGHT** = `16777216` `🔗<class_Image_constant_MAX_HEIGHT>`

The maximal height allowed for **Image** resources.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Dictionary<class_Dictionary>` **data** =
`{ "data": PackedByteArray(), "format": "Lum8", "height": 0, "mipmaps": false, "width": 0 }`
`🔗<class_Image_property_data>`

Holds all the image's color data in a given format. See
`Format<enum_Image_Format>` constants.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **adjust\_bcs**(brightness:
`float<class_float>`, contrast: `float<class_float>`, saturation:
`float<class_float>`) `🔗<class_Image_method_adjust_bcs>`

Adjusts this image's `brightness`, `contrast`, and `saturation` by the
given values. Does not work if the image is compressed (see
`is_compressed<class_Image_method_is_compressed>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **blend\_rect**(src: `Image<class_Image>`,
src\_rect: `Rect2i<class_Rect2i>`, dst: `Vector2i<class_Vector2i>`)
`🔗<class_Image_method_blend_rect>`

Alpha-blends `src_rect` from `src` image to this image at coordinates
`dst`, clipped accordingly to both image bounds. This image and `src`
image **must** have the same format. `src_rect` with non-positive size
is treated as empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **blend\_rect\_mask**(src:
`Image<class_Image>`, mask: `Image<class_Image>`, src\_rect:
`Rect2i<class_Rect2i>`, dst: `Vector2i<class_Vector2i>`)
`🔗<class_Image_method_blend_rect_mask>`

Alpha-blends `src_rect` from `src` image to this image using `mask`
image at coordinates `dst`, clipped accordingly to both image bounds.
Alpha channels are required for both `src` and `mask`. `dst` pixels and
`src` pixels will blend if the corresponding mask pixel's alpha value is
not 0. This image and `src` image **must** have the same format. `src`
image and `mask` image **must** have the same size (width and height)
but they can have different formats. `src_rect` with non-positive size
is treated as empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **blit\_rect**(src: `Image<class_Image>`,
src\_rect: `Rect2i<class_Rect2i>`, dst: `Vector2i<class_Vector2i>`)
`🔗<class_Image_method_blit_rect>`

Copies `src_rect` from `src` image to this image at coordinates `dst`,
clipped accordingly to both image bounds. This image and `src` image
**must** have the same format. `src_rect` with non-positive size is
treated as empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **blit\_rect\_mask**(src:
`Image<class_Image>`, mask: `Image<class_Image>`, src\_rect:
`Rect2i<class_Rect2i>`, dst: `Vector2i<class_Vector2i>`)
`🔗<class_Image_method_blit_rect_mask>`

Blits `src_rect` area from `src` image to this image at the coordinates
given by `dst`, clipped accordingly to both image bounds. `src` pixel is
copied onto `dst` if the corresponding `mask` pixel's alpha value is not
0. This image and `src` image **must** have the same format. `src` image
and `mask` image **must** have the same size (width and height) but they
can have different formats. `src_rect` with non-positive size is treated
as empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **bump\_map\_to\_normal\_map**(bump\_scale:
`float<class_float>` = 1.0)
`🔗<class_Image_method_bump_map_to_normal_map>`

Converts a bump map to a normal map. A bump map provides a height offset
per-pixel, while a normal map provides a normal direction per pixel.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_mipmaps**()
`🔗<class_Image_method_clear_mipmaps>`

Removes the image's mipmaps.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **compress**(mode:
`CompressMode<enum_Image_CompressMode>`, source:
`CompressSource<enum_Image_CompressSource>` = 0, astc\_format:
`ASTCFormat<enum_Image_ASTCFormat>` = 0)
`🔗<class_Image_method_compress>`

Compresses the image to use less memory. Can not directly access pixel
data while the image is compressed. Returns error if the chosen
compression mode is not available.

The `source` parameter helps to pick the best compression method for DXT
and ETC2 formats. It is ignored for ASTC compression.

For ASTC compression, the `astc_format` parameter must be supplied.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **compress\_from\_channels**(mode:
`CompressMode<enum_Image_CompressMode>`, channels:
`UsedChannels<enum_Image_UsedChannels>`, astc\_format:
`ASTCFormat<enum_Image_ASTCFormat>` = 0)
`🔗<class_Image_method_compress_from_channels>`

Compresses the image to use less memory. Can not directly access pixel
data while the image is compressed. Returns error if the chosen
compression mode is not available.

This is an alternative to `compress<class_Image_method_compress>` that
lets the user supply the channels used in order for the compressor to
pick the best DXT and ETC2 formats. For other formats (non DXT or ETC2),
this argument is ignored.

For ASTC compression, the `astc_format` parameter must be supplied.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**compute\_image\_metrics**(compared\_image: `Image<class_Image>`,
use\_luma: `bool<class_bool>`)
`🔗<class_Image_method_compute_image_metrics>`

Compute image metrics on the current image and the compared image.

The dictionary contains `max`, `mean`, `mean_squared`,
`root_mean_squared` and `peak_snr`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **convert**(format:
`Format<enum_Image_Format>`) `🔗<class_Image_method_convert>`

Converts the image's format. See `Format<enum_Image_Format>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **copy\_from**(src: `Image<class_Image>`)
`🔗<class_Image_method_copy_from>`

Copies `src` image to this image.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **create**(width: `int<class_int>`, height:
`int<class_int>`, use\_mipmaps: `bool<class_bool>`, format:
`Format<enum_Image_Format>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_Image_method_create>`

**Deprecated:** Use `create_empty<class_Image_method_create_empty>`.

Creates an empty image of given size and format. See
`Format<enum_Image_Format>` constants. If `use_mipmaps` is `true`, then
generate mipmaps for this image. See the
`generate_mipmaps<class_Image_method_generate_mipmaps>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **create\_empty**(width: `int<class_int>`, height:
`int<class_int>`, use\_mipmaps: `bool<class_bool>`, format:
`Format<enum_Image_Format>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_Image_method_create_empty>`

Creates an empty image of given size and format. See
`Format<enum_Image_Format>` constants. If `use_mipmaps` is `true`, then
generate mipmaps for this image. See the
`generate_mipmaps<class_Image_method_generate_mipmaps>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **create\_from\_data**(width: `int<class_int>`,
height: `int<class_int>`, use\_mipmaps: `bool<class_bool>`, format:
`Format<enum_Image_Format>`, data:
`PackedByteArray<class_PackedByteArray>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_Image_method_create_from_data>`

Creates a new image of given size and format. See
`Format<enum_Image_Format>` constants. Fills the image with the given
raw data. If `use_mipmaps` is `true` then loads mipmaps for this image
from `data`. See
`generate_mipmaps<class_Image_method_generate_mipmaps>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **crop**(width: `int<class_int>`, height:
`int<class_int>`) `🔗<class_Image_method_crop>`

Crops the image to the given `width` and `height`. If the specified size
is larger than the current size, the extra area is filled with black
pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **decompress**()
`🔗<class_Image_method_decompress>`

Decompresses the image if it is VRAM compressed in a supported format.
Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` if the format
is supported, otherwise
`@GlobalScope.ERR_UNAVAILABLE<class_@GlobalScope_constant_ERR_UNAVAILABLE>`.

\*\*Note:\*\* The following formats can be decompressed: DXT, RGTC,
BPTC. The formats ETC1 and ETC2 are not supported.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AlphaMode<enum_Image_AlphaMode>` **detect\_alpha**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_detect_alpha>`

Returns `ALPHA_BLEND<class_Image_constant_ALPHA_BLEND>` if the image has
data for alpha values. Returns
`ALPHA_BIT<class_Image_constant_ALPHA_BIT>` if all the alpha values are
stored in a single bit. Returns
`ALPHA_NONE<class_Image_constant_ALPHA_NONE>` if no data for alpha
values is found.

classref-item-separator

------------------------------------------------------------------------

classref-method

`UsedChannels<enum_Image_UsedChannels>`
**detect\_used\_channels**(source:
`CompressSource<enum_Image_CompressSource>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_detect_used_channels>`

Returns the color channels used by this image, as one of the
`UsedChannels<enum_Image_UsedChannels>` constants. If the image is
compressed, the original `source` must be specified.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fill**(color: `Color<class_Color>`)
`🔗<class_Image_method_fill>`

Fills the image with `color`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fill\_rect**(rect: `Rect2i<class_Rect2i>`,
color: `Color<class_Color>`) `🔗<class_Image_method_fill_rect>`

Fills `rect` with `color`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fix\_alpha\_edges**()
`🔗<class_Image_method_fix_alpha_edges>`

Blends low-alpha pixels with nearby pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **flip\_x**() `🔗<class_Image_method_flip_x>`

Flips the image horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **flip\_y**() `🔗<class_Image_method_flip_y>`

Flips the image vertically.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **generate\_mipmaps**(renormalize:
`bool<class_bool>` = false) `🔗<class_Image_method_generate_mipmaps>`

Generates mipmaps for the image. Mipmaps are precalculated
lower-resolution copies of the image that are automatically used if the
image needs to be scaled down when rendered. They help improve image
quality and performance when rendering. This method returns an error if
the image is compressed, in a custom format, or if the image's
width/height is `0`. Enabling `renormalize` when generating mipmaps for
normal map textures will make sure all resulting vector values are
normalized.

It is possible to check if the image has mipmaps by calling
`has_mipmaps<class_Image_method_has_mipmaps>` or
`get_mipmap_count<class_Image_method_get_mipmap_count>`. Calling
`generate_mipmaps<class_Image_method_generate_mipmaps>` on an image that
already has mipmaps will replace existing mipmaps in the image.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **get\_data**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_data>`

Returns a copy of the image's raw data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_data\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_data_size>`

Returns size (in bytes) of the image's raw data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Format<enum_Image_Format>` **get\_format**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_format>`

Returns the image's format. See `Format<enum_Image_Format>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_height**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_height>`

Returns the image's height.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_mipmap\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_mipmap_count>`

Returns the number of mipmap levels or 0 if the image has no mipmaps.
The largest main level image is not counted as a mipmap level by this
method, so if you want to include it you can add 1 to this count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_mipmap\_offset**(mipmap: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_mipmap_offset>`

Returns the offset where the image's mipmap with index `mipmap` is
stored in the `data<class_Image_property_data>` dictionary.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_pixel**(x: `int<class_int>`, y:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_pixel>`

Returns the color of the pixel at `(x, y)`.

This is the same as `get_pixelv<class_Image_method_get_pixelv>`, but
with two integer arguments instead of a `Vector2i<class_Vector2i>`
argument.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_pixelv**(point: `Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_pixelv>`

Returns the color of the pixel at `point`.

This is the same as `get_pixel<class_Image_method_get_pixel>`, but with
a `Vector2i<class_Vector2i>` argument instead of two integer arguments.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **get\_region**(region: `Rect2i<class_Rect2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_region>`

Returns a new **Image** that is a copy of this **Image**'s area
specified with `region`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_size>`

Returns the image's size (width and height).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2i<class_Rect2i>` **get\_used\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_used_rect>`

Returns a `Rect2i<class_Rect2i>` enclosing the visible portion of the
image, considering each pixel with a non-zero alpha channel as visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_width**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_get_width>`

Returns the image's width.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_mipmaps**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_has_mipmaps>`

Returns `true` if the image has generated mipmaps.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_compressed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_is_compressed>`

Returns `true` if the image is compressed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_empty**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_is_empty>`

Returns `true` if the image has no data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_invisible**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_is_invisible>`

Returns `true` if all the image's pixels have an alpha value of 0.
Returns `false` if any pixel has an alpha value higher than 0.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **linear\_to\_srgb**()
`🔗<class_Image_method_linear_to_srgb>`

Converts the entire image from the linear colorspace to the sRGB
colorspace. Only works on images with
`FORMAT_RGB8<class_Image_constant_FORMAT_RGB8>` or
`FORMAT_RGBA8<class_Image_constant_FORMAT_RGBA8>` formats.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load**(path: `String<class_String>`)
`🔗<class_Image_method_load>`

Loads an image from file `path`. See [Supported image
formats](../tutorials/assets_pipeline/importing_images.html#supported-image-formats)
for a list of supported image formats and limitations.

\*\*Warning:\*\* This method should only be used in the editor or in
cases when you need to load external images at run-time, such as images
located at the `user://` directory, and may not work in exported
projects.

See also `ImageTexture<class_ImageTexture>` description for usage
examples.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_bmp\_from\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Image_method_load_bmp_from_buffer>`

Loads an image from the binary contents of a BMP file.

\*\*Note:\*\* Godot's BMP module doesn't support 16-bit per pixel
images. Only 1-bit, 4-bit, 8-bit, 24-bit, and 32-bit per pixel images
are supported.

\*\*Note:\*\* This method is only available in engine builds with the
BMP module enabled. By default, the BMP module is enabled, but it can be
disabled at build-time using the `module_bmp_enabled=no` SCons option.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **load\_from\_file**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_Image_method_load_from_file>`

Creates a new **Image** and loads data from the specified file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_jpg\_from\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Image_method_load_jpg_from_buffer>`

Loads an image from the binary contents of a JPEG file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_ktx\_from\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Image_method_load_ktx_from_buffer>`

Loads an image from the binary contents of a
[KTX](https://github.com/KhronosGroup/KTX-Software) file. Unlike most
image formats, KTX can store VRAM-compressed data and embed mipmaps.

\*\*Note:\*\* Godot's libktx implementation only supports 2D images.
Cubemaps, texture arrays, and de-padding are not supported.

\*\*Note:\*\* This method is only available in engine builds with the
KTX module enabled. By default, the KTX module is enabled, but it can be
disabled at build-time using the `module_ktx_enabled=no` SCons option.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_png\_from\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Image_method_load_png_from_buffer>`

Loads an image from the binary contents of a PNG file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_svg\_from\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`, scale: `float<class_float>` =
1.0) `🔗<class_Image_method_load_svg_from_buffer>`

Loads an image from the UTF-8 binary contents of an **uncompressed** SVG
file (**.svg**).

\*\*Note:\*\* Beware when using compressed SVG files (like **.svgz**),
they need to be `decompressed` before loading.

\*\*Note:\*\* This method is only available in engine builds with the
SVG module enabled. By default, the SVG module is enabled, but it can be
disabled at build-time using the `module_svg_enabled=no` SCons option.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_svg\_from\_string**(svg\_str:
`String<class_String>`, scale: `float<class_float>` = 1.0)
`🔗<class_Image_method_load_svg_from_string>`

Loads an image from the string contents of an SVG file (**.svg**).

\*\*Note:\*\* This method is only available in engine builds with the
SVG module enabled. By default, the SVG module is enabled, but it can be
disabled at build-time using the `module_svg_enabled=no` SCons option.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_tga\_from\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Image_method_load_tga_from_buffer>`

Loads an image from the binary contents of a TGA file.

\*\*Note:\*\* This method is only available in engine builds with the
TGA module enabled. By default, the TGA module is enabled, but it can be
disabled at build-time using the `module_tga_enabled=no` SCons option.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_webp\_from\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Image_method_load_webp_from_buffer>`

Loads an image from the binary contents of a WebP file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **normal\_map\_to\_xy**()
`🔗<class_Image_method_normal_map_to_xy>`

Converts the image's data to represent coordinates on a 3D plane. This
is used when the image represents a normal map. A normal map can add
lots of detail to a 3D surface without increasing the polygon count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **premultiply\_alpha**()
`🔗<class_Image_method_premultiply_alpha>`

Multiplies color values with alpha values. Resulting color values for a
pixel are `(color * alpha)/256`. See also
`CanvasItemMaterial.blend_mode<class_CanvasItemMaterial_property_blend_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **resize**(width: `int<class_int>`, height:
`int<class_int>`, interpolation:
`Interpolation<enum_Image_Interpolation>` = 1)
`🔗<class_Image_method_resize>`

Resizes the image to the given `width` and `height`. New pixels are
calculated using the `interpolation` mode defined via
`Interpolation<enum_Image_Interpolation>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **resize\_to\_po2**(square: `bool<class_bool>`
= false, interpolation: `Interpolation<enum_Image_Interpolation>` = 1)
`🔗<class_Image_method_resize_to_po2>`

Resizes the image to the nearest power of 2 for the width and height. If
`square` is `true` then set width and height to be the same. New pixels
are calculated using the `interpolation` mode defined via
`Interpolation<enum_Image_Interpolation>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **rgbe\_to\_srgb**()
`🔗<class_Image_method_rgbe_to_srgb>`

Converts a standard RGBE (Red Green Blue Exponent) image to an sRGB
image.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rotate\_90**(direction:
`ClockDirection<enum_@GlobalScope_ClockDirection>`)
`🔗<class_Image_method_rotate_90>`

Rotates the image in the specified `direction` by `90` degrees. The
width and height of the image must be greater than `1`. If the width and
height are not equal, the image will be resized.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rotate\_180**()
`🔗<class_Image_method_rotate_180>`

Rotates the image by `180` degrees. The width and height of the image
must be greater than `1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save\_exr**(path:
`String<class_String>`, grayscale: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_save_exr>`

Saves the image as an EXR file to `path`. If `grayscale` is `true` and
the image has only one channel, it will be saved explicitly as
monochrome rather than one red channel. This function will return
`@GlobalScope.ERR_UNAVAILABLE<class_@GlobalScope_constant_ERR_UNAVAILABLE>`
if Godot was compiled without the TinyEXR module.

\*\*Note:\*\* The TinyEXR module is disabled in non-editor builds, which
means `save_exr<class_Image_method_save_exr>` will return
`@GlobalScope.ERR_UNAVAILABLE<class_@GlobalScope_constant_ERR_UNAVAILABLE>`
when it is called from an exported project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**save\_exr\_to\_buffer**(grayscale: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_save_exr_to_buffer>`

Saves the image as an EXR file to a byte array. If `grayscale` is `true`
and the image has only one channel, it will be saved explicitly as
monochrome rather than one red channel. This function will return an
empty byte array if Godot was compiled without the TinyEXR module.

\*\*Note:\*\* The TinyEXR module is disabled in non-editor builds, which
means `save_exr<class_Image_method_save_exr>` will return an empty byte
array when it is called from an exported project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save\_jpg**(path:
`String<class_String>`, quality: `float<class_float>` = 0.75)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_save_jpg>`

Saves the image as a JPEG file to `path` with the specified `quality`
between `0.01` and `1.0` (inclusive). Higher `quality` values result in
better-looking output at the cost of larger file sizes. Recommended
`quality` values are between `0.75` and `0.90`. Even at quality `1.00`,
JPEG compression remains lossy.

\*\*Note:\*\* JPEG does not save an alpha channel. If the **Image**
contains an alpha channel, the image will still be saved, but the
resulting JPEG file won't contain the alpha channel.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**save\_jpg\_to\_buffer**(quality: `float<class_float>` = 0.75)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_save_jpg_to_buffer>`

Saves the image as a JPEG file to a byte array with the specified
`quality` between `0.01` and `1.0` (inclusive). Higher `quality` values
result in better-looking output at the cost of larger byte array sizes
(and therefore memory usage). Recommended `quality` values are between
`0.75` and `0.90`. Even at quality `1.00`, JPEG compression remains
lossy.

\*\*Note:\*\* JPEG does not save an alpha channel. If the **Image**
contains an alpha channel, the image will still be saved, but the
resulting byte array won't contain the alpha channel.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save\_png**(path:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_save_png>`

Saves the image as a PNG file to the file at `path`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **save\_png\_to\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_save_png_to_buffer>`

Saves the image as a PNG file to a byte array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save\_webp**(path:
`String<class_String>`, lossy: `bool<class_bool>` = false, quality:
`float<class_float>` = 0.75)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_save_webp>`

Saves the image as a WebP (Web Picture) file to the file at `path`. By
default it will save lossless. If `lossy` is true, the image will be
saved lossy, using the `quality` setting between 0.0 and 1.0
(inclusive). Lossless WebP offers more efficient compression than PNG.

\*\*Note:\*\* The WebP format is limited to a size of 16383×16383
pixels, while PNG can save larger images.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**save\_webp\_to\_buffer**(lossy: `bool<class_bool>` = false, quality:
`float<class_float>` = 0.75)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Image_method_save_webp_to_buffer>`

Saves the image as a WebP (Web Picture) file to a byte array. By default
it will save lossless. If `lossy` is true, the image will be saved
lossy, using the `quality` setting between 0.0 and 1.0 (inclusive).
Lossless WebP offers more efficient compression than PNG.

\*\*Note:\*\* The WebP format is limited to a size of 16383×16383
pixels, while PNG can save larger images.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_data**(width: `int<class_int>`, height:
`int<class_int>`, use\_mipmaps: `bool<class_bool>`, format:
`Format<enum_Image_Format>`, data:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Image_method_set_data>`

Overwrites data of an existing **Image**. Non-static equivalent of
`create_from_data<class_Image_method_create_from_data>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_pixel**(x: `int<class_int>`, y:
`int<class_int>`, color: `Color<class_Color>`)
`🔗<class_Image_method_set_pixel>`

Sets the `Color<class_Color>` of the pixel at `(x, y)` to `color`.

gdscript

var img\_width = 10 var img\_height = 5 var img =
Image.create(img\_width, img\_height, false, Image.FORMAT\_RGBA8)

img.set\_pixel(1, 2, Color.RED) \# Sets the color at (1, 2) to red.

csharp

int imgWidth = 10; int imgHeight = 5; var img = Image.Create(imgWidth,
imgHeight, false, Image.Format.Rgba8);

img.SetPixel(1, 2, Colors.Red); // Sets the color at (1, 2) to red.

This is the same as `set_pixelv<class_Image_method_set_pixelv>`, but
with a two integer arguments instead of a `Vector2i<class_Vector2i>`
argument.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_pixelv**(point:
`Vector2i<class_Vector2i>`, color: `Color<class_Color>`)
`🔗<class_Image_method_set_pixelv>`

Sets the `Color<class_Color>` of the pixel at `point` to `color`.

gdscript

var img\_width = 10 var img\_height = 5 var img =
Image.create(img\_width, img\_height, false, Image.FORMAT\_RGBA8)

img.set\_pixelv(Vector2i(1, 2), Color.RED) \# Sets the color at (1, 2)
to red.

csharp

int imgWidth = 10; int imgHeight = 5; var img = Image.Create(imgWidth,
imgHeight, false, Image.Format.Rgba8);

img.SetPixelv(new Vector2I(1, 2), Colors.Red); // Sets the color at (1,
2) to red.

This is the same as `set_pixel<class_Image_method_set_pixel>`, but with
a `Vector2i<class_Vector2i>` argument instead of two integer arguments.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **shrink\_x2**()
`🔗<class_Image_method_shrink_x2>`

Shrinks the image by a factor of 2 on each axis (this divides the pixel
count by 4).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **srgb\_to\_linear**()
`🔗<class_Image_method_srgb_to_linear>`

Converts the raw data from the sRGB colorspace to a linear scale. Only
works on images with `FORMAT_RGB8<class_Image_constant_FORMAT_RGB8>` or
`FORMAT_RGBA8<class_Image_constant_FORMAT_RGBA8>` formats.
