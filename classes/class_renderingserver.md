github\_url  
hide

# RenderingServer

**Inherits:** `Object<class_Object>`

Server for anything visible.

classref-introduction-group

## Description

The rendering server is the API backend for everything visible. The
whole scene system mounts on it to display. The rendering server is
completely opaque: the internals are entirely implementation-specific
and cannot be accessed.

The rendering server can be used to bypass the scene/`Node<class_Node>`
system entirely. This can improve performance in cases where the scene
system is the bottleneck, but won't improve performance otherwise (for
instance, if the GPU is already fully utilized).

Resources are created using the `*_create` functions. These functions
return `RID<class_RID>`s which are not references to the objects
themselves, but opaque *pointers* towards these objects.

All objects are drawn to a viewport. You can use the
`Viewport<class_Viewport>` attached to the `SceneTree<class_SceneTree>`
or you can create one yourself with
`viewport_create<class_RenderingServer_method_viewport_create>`. When
using a custom scenario or canvas, the scenario or canvas needs to be
attached to the viewport using
`viewport_set_scenario<class_RenderingServer_method_viewport_set_scenario>`
or
`viewport_attach_canvas<class_RenderingServer_method_viewport_attach_canvas>`.

\*\*Scenarios:\*\* In 3D, all visual objects must be associated with a
scenario. The scenario is a visual representation of the world. If
accessing the rendering server from a running game, the scenario can be
accessed from the scene tree from any `Node3D<class_Node3D>` node with
`Node3D.get_world_3d<class_Node3D_method_get_world_3d>`. Otherwise, a
scenario can be created with
`scenario_create<class_RenderingServer_method_scenario_create>`.

Similarly, in 2D, a canvas is needed to draw all canvas items.

\*\*3D:\*\* In 3D, all visible objects are comprised of a resource and
an instance. A resource can be a mesh, a particle system, a light, or
any other 3D object. In order to be visible resources must be attached
to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`. The
instance must also be attached to the scenario using
`instance_set_scenario<class_RenderingServer_method_instance_set_scenario>`
in order to be visible. RenderingServer methods that don't have a prefix
are usually 3D-specific (but not always).

\*\*2D:\*\* In 2D, all visible objects are some form of canvas item. In
order to be visible, a canvas item needs to be the child of a canvas
attached to a viewport, or it needs to be the child of another canvas
item that is eventually attached to the canvas. 2D-specific
RenderingServer methods generally start with `canvas_*`.

\*\*Headless mode:\*\* Starting the engine with the `--headless`
`command line argument <../tutorials/editor/command_line_tutorial>`
disables all rendering and window management functions. Most functions
from **RenderingServer** will return dummy values in this case.

classref-introduction-group

## Tutorials

-   `Optimization using Servers <../tutorials/performance/using_servers>`

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

**frame\_post\_draw**()
`🔗<class_RenderingServer_signal_frame_post_draw>`

Emitted at the end of the frame, after the RenderingServer has finished
updating all the Viewports.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**frame\_pre\_draw**() `🔗<class_RenderingServer_signal_frame_pre_draw>`

Emitted at the beginning of the frame, before the RenderingServer
updates all the Viewports.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TextureType**: `🔗<enum_RenderingServer_TextureType>`

classref-enumeration-constant

`TextureType<enum_RenderingServer_TextureType>` **TEXTURE\_TYPE\_2D** =
`0`

2D texture.

classref-enumeration-constant

`TextureType<enum_RenderingServer_TextureType>`
**TEXTURE\_TYPE\_LAYERED** = `1`

Layered texture.

classref-enumeration-constant

`TextureType<enum_RenderingServer_TextureType>` **TEXTURE\_TYPE\_3D** =
`2`

3D texture.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureLayeredType**:
`🔗<enum_RenderingServer_TextureLayeredType>`

classref-enumeration-constant

`TextureLayeredType<enum_RenderingServer_TextureLayeredType>`
**TEXTURE\_LAYERED\_2D\_ARRAY** = `0`

Array of 2-dimensional textures (see
`Texture2DArray<class_Texture2DArray>`).

classref-enumeration-constant

`TextureLayeredType<enum_RenderingServer_TextureLayeredType>`
**TEXTURE\_LAYERED\_CUBEMAP** = `1`

Cubemap texture (see `Cubemap<class_Cubemap>`).

classref-enumeration-constant

`TextureLayeredType<enum_RenderingServer_TextureLayeredType>`
**TEXTURE\_LAYERED\_CUBEMAP\_ARRAY** = `2`

Array of cubemap textures (see `CubemapArray<class_CubemapArray>`).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CubeMapLayer**: `🔗<enum_RenderingServer_CubeMapLayer>`

classref-enumeration-constant

`CubeMapLayer<enum_RenderingServer_CubeMapLayer>`
**CUBEMAP\_LAYER\_LEFT** = `0`

Left face of a `Cubemap<class_Cubemap>`.

classref-enumeration-constant

`CubeMapLayer<enum_RenderingServer_CubeMapLayer>`
**CUBEMAP\_LAYER\_RIGHT** = `1`

Right face of a `Cubemap<class_Cubemap>`.

classref-enumeration-constant

`CubeMapLayer<enum_RenderingServer_CubeMapLayer>`
**CUBEMAP\_LAYER\_BOTTOM** = `2`

Bottom face of a `Cubemap<class_Cubemap>`.

classref-enumeration-constant

`CubeMapLayer<enum_RenderingServer_CubeMapLayer>`
**CUBEMAP\_LAYER\_TOP** = `3`

Top face of a `Cubemap<class_Cubemap>`.

classref-enumeration-constant

`CubeMapLayer<enum_RenderingServer_CubeMapLayer>`
**CUBEMAP\_LAYER\_FRONT** = `4`

Front face of a `Cubemap<class_Cubemap>`.

classref-enumeration-constant

`CubeMapLayer<enum_RenderingServer_CubeMapLayer>`
**CUBEMAP\_LAYER\_BACK** = `5`

Back face of a `Cubemap<class_Cubemap>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ShaderMode**: `🔗<enum_RenderingServer_ShaderMode>`

classref-enumeration-constant

`ShaderMode<enum_RenderingServer_ShaderMode>` **SHADER\_SPATIAL** = `0`

Shader is a 3D shader.

classref-enumeration-constant

`ShaderMode<enum_RenderingServer_ShaderMode>` **SHADER\_CANVAS\_ITEM** =
`1`

Shader is a 2D shader.

classref-enumeration-constant

`ShaderMode<enum_RenderingServer_ShaderMode>` **SHADER\_PARTICLES** =
`2`

Shader is a particle shader (can be used in both 2D and 3D).

classref-enumeration-constant

`ShaderMode<enum_RenderingServer_ShaderMode>` **SHADER\_SKY** = `3`

Shader is a 3D sky shader.

classref-enumeration-constant

`ShaderMode<enum_RenderingServer_ShaderMode>` **SHADER\_FOG** = `4`

Shader is a 3D fog shader.

classref-enumeration-constant

`ShaderMode<enum_RenderingServer_ShaderMode>` **SHADER\_MAX** = `5`

Represents the size of the `ShaderMode<enum_RenderingServer_ShaderMode>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ArrayType**: `🔗<enum_RenderingServer_ArrayType>`

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_VERTEX** = `0`

Array is a vertex position array.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_NORMAL** = `1`

Array is a normal array.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_TANGENT** = `2`

Array is a tangent array.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_COLOR** = `3`

Array is a vertex color array.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_TEX\_UV** = `4`

Array is a UV coordinates array.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_TEX\_UV2** = `5`

Array is a UV coordinates array for the second set of UV coordinates.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_CUSTOM0** = `6`

Array is a custom data array for the first set of custom data.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_CUSTOM1** = `7`

Array is a custom data array for the second set of custom data.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_CUSTOM2** = `8`

Array is a custom data array for the third set of custom data.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_CUSTOM3** = `9`

Array is a custom data array for the fourth set of custom data.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_BONES** = `10`

Array contains bone information.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_WEIGHTS** = `11`

Array is weight information.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_INDEX** = `12`

Array is an index array.

classref-enumeration-constant

`ArrayType<enum_RenderingServer_ArrayType>` **ARRAY\_MAX** = `13`

Represents the size of the `ArrayType<enum_RenderingServer_ArrayType>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ArrayCustomFormat**: `🔗<enum_RenderingServer_ArrayCustomFormat>`

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_RGBA8\_UNORM** = `0`

Custom data array contains 8-bit-per-channel red/green/blue/alpha color
data. Values are normalized, unsigned floating-point in the `[0.0, 1.0]`
range.

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_RGBA8\_SNORM** = `1`

Custom data array contains 8-bit-per-channel red/green/blue/alpha color
data. Values are normalized, signed floating-point in the `[-1.0, 1.0]`
range.

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_RG\_HALF** = `2`

Custom data array contains 16-bit-per-channel red/green color data.
Values are floating-point in half precision.

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_RGBA\_HALF** = `3`

Custom data array contains 16-bit-per-channel red/green/blue/alpha color
data. Values are floating-point in half precision.

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_R\_FLOAT** = `4`

Custom data array contains 32-bit-per-channel red color data. Values are
floating-point in single precision.

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_RG\_FLOAT** = `5`

Custom data array contains 32-bit-per-channel red/green color data.
Values are floating-point in single precision.

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_RGB\_FLOAT** = `6`

Custom data array contains 32-bit-per-channel red/green/blue color data.
Values are floating-point in single precision.

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_RGBA\_FLOAT** = `7`

Custom data array contains 32-bit-per-channel red/green/blue/alpha color
data. Values are floating-point in single precision.

classref-enumeration-constant

`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>`
**ARRAY\_CUSTOM\_MAX** = `8`

Represents the size of the
`ArrayCustomFormat<enum_RenderingServer_ArrayCustomFormat>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **ArrayFormat**: `🔗<enum_RenderingServer_ArrayFormat>`

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_VERTEX** = `1`

Flag used to mark a vertex position array.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_NORMAL** = `2`

Flag used to mark a normal array.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_TANGENT** = `4`

Flag used to mark a tangent array.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>` **ARRAY\_FORMAT\_COLOR**
= `8`

Flag used to mark a vertex color array.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_TEX\_UV** = `16`

Flag used to mark a UV coordinates array.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_TEX\_UV2** = `32`

Flag used to mark a UV coordinates array for the second UV coordinates.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM0** = `64`

Flag used to mark an array of custom per-vertex data for the first set
of custom data.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM1** = `128`

Flag used to mark an array of custom per-vertex data for the second set
of custom data.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM2** = `256`

Flag used to mark an array of custom per-vertex data for the third set
of custom data.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM3** = `512`

Flag used to mark an array of custom per-vertex data for the fourth set
of custom data.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>` **ARRAY\_FORMAT\_BONES**
= `1024`

Flag used to mark a bone information array.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_WEIGHTS** = `2048`

Flag used to mark a weights array.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>` **ARRAY\_FORMAT\_INDEX**
= `4096`

Flag used to mark an index array.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_BLEND\_SHAPE\_MASK** = `7`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM\_BASE** = `13`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM\_BITS** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM0\_SHIFT** = `13`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM1\_SHIFT** = `16`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM2\_SHIFT** = `19`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM3\_SHIFT** = `22`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FORMAT\_CUSTOM\_MASK** = `7`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_COMPRESS\_FLAGS\_BASE** = `25`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_USE\_2D\_VERTICES** = `33554432`

Flag used to mark that the array contains 2D vertices.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_USE\_DYNAMIC\_UPDATE** = `67108864`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_USE\_8\_BONE\_WEIGHTS** = `134217728`

Flag used to mark that the array uses 8 bone weights instead of 4.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_USES\_EMPTY\_VERTEX\_ARRAY** = `268435456`

Flag used to mark that the mesh does not have a vertex array and instead
will infer vertex positions in the shader using indices and other
information.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_COMPRESS\_ATTRIBUTES** = `536870912`

Flag used to mark that a mesh is using compressed attributes (vertices,
normals, tangents, UVs). When this form of compression is enabled,
vertex positions will be packed into an RGBA16UNORM attribute and scaled
in the vertex shader. The normal and tangent will be packed into an
RG16UNORM representing an axis, and a 16-bit float stored in the
A-channel of the vertex. UVs will use 16-bit normalized floats instead
of full 32-bit signed floats. When using this compression mode you must
use either vertices, normals, and tangents or only vertices. You cannot
use normals without tangents. Importers will automatically enable this
compression if they can.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_FORMAT\_VERSION\_BASE** = `35`

Flag used to mark the start of the bits used to store the mesh version.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_FORMAT\_VERSION\_SHIFT** = `35`

Flag used to shift a mesh format int to bring the version into the
lowest digits.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_FORMAT\_VERSION\_1** = `0`

Flag used to record the format used by prior mesh versions before the
introduction of a version.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_FORMAT\_VERSION\_2** = `34359738368`

Flag used to record the second iteration of the mesh version flag. The
primary difference between this and
`ARRAY_FLAG_FORMAT_VERSION_1<class_RenderingServer_constant_ARRAY_FLAG_FORMAT_VERSION_1>`
is that this version supports
`ARRAY_FLAG_COMPRESS_ATTRIBUTES<class_RenderingServer_constant_ARRAY_FLAG_COMPRESS_ATTRIBUTES>`
and in this version vertex positions are de-interleaved from normals and
tangents.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_FORMAT\_CURRENT\_VERSION** = `34359738368`

Flag used to record the current version that the engine expects.
Currently this is the same as
`ARRAY_FLAG_FORMAT_VERSION_2<class_RenderingServer_constant_ARRAY_FLAG_FORMAT_VERSION_2>`.

classref-enumeration-constant

`ArrayFormat<enum_RenderingServer_ArrayFormat>`
**ARRAY\_FLAG\_FORMAT\_VERSION\_MASK** = `255`

Flag used to isolate the bits used for mesh version after using
`ARRAY_FLAG_FORMAT_VERSION_SHIFT<class_RenderingServer_constant_ARRAY_FLAG_FORMAT_VERSION_SHIFT>`
to shift them into place.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PrimitiveType**: `🔗<enum_RenderingServer_PrimitiveType>`

classref-enumeration-constant

`PrimitiveType<enum_RenderingServer_PrimitiveType>`
**PRIMITIVE\_POINTS** = `0`

Primitive to draw consists of points.

classref-enumeration-constant

`PrimitiveType<enum_RenderingServer_PrimitiveType>` **PRIMITIVE\_LINES**
= `1`

Primitive to draw consists of lines.

classref-enumeration-constant

`PrimitiveType<enum_RenderingServer_PrimitiveType>`
**PRIMITIVE\_LINE\_STRIP** = `2`

Primitive to draw consists of a line strip from start to end.

classref-enumeration-constant

`PrimitiveType<enum_RenderingServer_PrimitiveType>`
**PRIMITIVE\_TRIANGLES** = `3`

Primitive to draw consists of triangles.

classref-enumeration-constant

`PrimitiveType<enum_RenderingServer_PrimitiveType>`
**PRIMITIVE\_TRIANGLE\_STRIP** = `4`

Primitive to draw consists of a triangle strip (the last 3 vertices are
always combined to make a triangle).

classref-enumeration-constant

`PrimitiveType<enum_RenderingServer_PrimitiveType>` **PRIMITIVE\_MAX** =
`5`

Represents the size of the
`PrimitiveType<enum_RenderingServer_PrimitiveType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BlendShapeMode**: `🔗<enum_RenderingServer_BlendShapeMode>`

classref-enumeration-constant

`BlendShapeMode<enum_RenderingServer_BlendShapeMode>`
**BLEND\_SHAPE\_MODE\_NORMALIZED** = `0`

Blend shapes are normalized.

classref-enumeration-constant

`BlendShapeMode<enum_RenderingServer_BlendShapeMode>`
**BLEND\_SHAPE\_MODE\_RELATIVE** = `1`

Blend shapes are relative to base weight.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MultimeshTransformFormat**:
`🔗<enum_RenderingServer_MultimeshTransformFormat>`

classref-enumeration-constant

`MultimeshTransformFormat<enum_RenderingServer_MultimeshTransformFormat>`
**MULTIMESH\_TRANSFORM\_2D** = `0`

Use `Transform2D<class_Transform2D>` to store MultiMesh transform.

classref-enumeration-constant

`MultimeshTransformFormat<enum_RenderingServer_MultimeshTransformFormat>`
**MULTIMESH\_TRANSFORM\_3D** = `1`

Use `Transform3D<class_Transform3D>` to store MultiMesh transform.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MultimeshPhysicsInterpolationQuality**:
`🔗<enum_RenderingServer_MultimeshPhysicsInterpolationQuality>`

classref-enumeration-constant

`MultimeshPhysicsInterpolationQuality<enum_RenderingServer_MultimeshPhysicsInterpolationQuality>`
**MULTIMESH\_INTERP\_QUALITY\_FAST** = `0`

MultiMesh physics interpolation favors speed over quality.

classref-enumeration-constant

`MultimeshPhysicsInterpolationQuality<enum_RenderingServer_MultimeshPhysicsInterpolationQuality>`
**MULTIMESH\_INTERP\_QUALITY\_HIGH** = `1`

MultiMesh physics interpolation favors quality over speed.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightProjectorFilter**:
`🔗<enum_RenderingServer_LightProjectorFilter>`

classref-enumeration-constant

`LightProjectorFilter<enum_RenderingServer_LightProjectorFilter>`
**LIGHT\_PROJECTOR\_FILTER\_NEAREST** = `0`

Nearest-neighbor filter for light projectors (use for pixel art light
projectors). No mipmaps are used for rendering, which means light
projectors at a distance will look sharp but grainy. This has roughly
the same performance cost as using mipmaps.

classref-enumeration-constant

`LightProjectorFilter<enum_RenderingServer_LightProjectorFilter>`
**LIGHT\_PROJECTOR\_FILTER\_LINEAR** = `1`

Linear filter for light projectors (use for non-pixel art light
projectors). No mipmaps are used for rendering, which means light
projectors at a distance will look smooth but blurry. This has roughly
the same performance cost as using mipmaps.

classref-enumeration-constant

`LightProjectorFilter<enum_RenderingServer_LightProjectorFilter>`
**LIGHT\_PROJECTOR\_FILTER\_NEAREST\_MIPMAPS** = `2`

Nearest-neighbor filter for light projectors (use for pixel art light
projectors). Isotropic mipmaps are used for rendering, which means light
projectors at a distance will look smooth but blurry. This has roughly
the same performance cost as not using mipmaps.

classref-enumeration-constant

`LightProjectorFilter<enum_RenderingServer_LightProjectorFilter>`
**LIGHT\_PROJECTOR\_FILTER\_LINEAR\_MIPMAPS** = `3`

Linear filter for light projectors (use for non-pixel art light
projectors). Isotropic mipmaps are used for rendering, which means light
projectors at a distance will look smooth but blurry. This has roughly
the same performance cost as not using mipmaps.

classref-enumeration-constant

`LightProjectorFilter<enum_RenderingServer_LightProjectorFilter>`
**LIGHT\_PROJECTOR\_FILTER\_NEAREST\_MIPMAPS\_ANISOTROPIC** = `4`

Nearest-neighbor filter for light projectors (use for pixel art light
projectors). Anisotropic mipmaps are used for rendering, which means
light projectors at a distance will look smooth and sharp when viewed
from oblique angles. This looks better compared to isotropic mipmaps,
but is slower. The level of anisotropic filtering is defined by
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

classref-enumeration-constant

`LightProjectorFilter<enum_RenderingServer_LightProjectorFilter>`
**LIGHT\_PROJECTOR\_FILTER\_LINEAR\_MIPMAPS\_ANISOTROPIC** = `5`

Linear filter for light projectors (use for non-pixel art light
projectors). Anisotropic mipmaps are used for rendering, which means
light projectors at a distance will look smooth and sharp when viewed
from oblique angles. This looks better compared to isotropic mipmaps,
but is slower. The level of anisotropic filtering is defined by
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightType**: `🔗<enum_RenderingServer_LightType>`

classref-enumeration-constant

`LightType<enum_RenderingServer_LightType>` **LIGHT\_DIRECTIONAL** = `0`

Directional (sun/moon) light (see
`DirectionalLight3D<class_DirectionalLight3D>`).

classref-enumeration-constant

`LightType<enum_RenderingServer_LightType>` **LIGHT\_OMNI** = `1`

Omni light (see `OmniLight3D<class_OmniLight3D>`).

classref-enumeration-constant

`LightType<enum_RenderingServer_LightType>` **LIGHT\_SPOT** = `2`

Spot light (see `SpotLight3D<class_SpotLight3D>`).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightParam**: `🔗<enum_RenderingServer_LightParam>`

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>` **LIGHT\_PARAM\_ENERGY** =
`0`

The light's energy multiplier.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_INDIRECT\_ENERGY** = `1`

The light's indirect energy multiplier (final indirect energy is
`LIGHT_PARAM_ENERGY<class_RenderingServer_constant_LIGHT_PARAM_ENERGY>`
\*
`LIGHT_PARAM_INDIRECT_ENERGY<class_RenderingServer_constant_LIGHT_PARAM_INDIRECT_ENERGY>`).

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_VOLUMETRIC\_FOG\_ENERGY** = `2`

The light's volumetric fog energy multiplier (final volumetric fog
energy is
`LIGHT_PARAM_ENERGY<class_RenderingServer_constant_LIGHT_PARAM_ENERGY>`
\*
`LIGHT_PARAM_VOLUMETRIC_FOG_ENERGY<class_RenderingServer_constant_LIGHT_PARAM_VOLUMETRIC_FOG_ENERGY>`).

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>` **LIGHT\_PARAM\_SPECULAR**
= `3`

The light's influence on specularity.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>` **LIGHT\_PARAM\_RANGE** =
`4`

The light's range.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>` **LIGHT\_PARAM\_SIZE** =
`5`

The size of the light when using spot light or omni light. The angular
size of the light when using directional light.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_ATTENUATION** = `6`

The light's attenuation.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SPOT\_ANGLE** = `7`

The spotlight's angle.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SPOT\_ATTENUATION** = `8`

The spotlight's attenuation.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_MAX\_DISTANCE** = `9`

The maximum distance for shadow splits. Increasing this value will make
directional shadows visible from further away, at the cost of lower
overall shadow detail and performance (since more objects need to be
included in the directional shadow rendering).

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_SPLIT\_1\_OFFSET** = `10`

Proportion of shadow atlas occupied by the first split.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_SPLIT\_2\_OFFSET** = `11`

Proportion of shadow atlas occupied by the second split.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_SPLIT\_3\_OFFSET** = `12`

Proportion of shadow atlas occupied by the third split. The fourth split
occupies the rest.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_FADE\_START** = `13`

Proportion of shadow max distance where the shadow will start to fade
out.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_NORMAL\_BIAS** = `14`

Normal bias used to offset shadow lookup by object normal. Can be used
to fix self-shadowing artifacts.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_BIAS** = `15`

Bias the shadow lookup to fix self-shadowing artifacts.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_PANCAKE\_SIZE** = `16`

Sets the size of the directional shadow pancake. The pancake offsets the
start of the shadow's camera frustum to provide a higher effective depth
resolution for the shadow. However, a high pancake size can cause
artifacts in the shadows of large objects that are close to the edge of
the frustum. Reducing the pancake size can help. Setting the size to `0`
turns off the pancaking effect.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_OPACITY** = `17`

The light's shadow opacity. Values lower than `1.0` make the light
appear through shadows. This can be used to fake global illumination at
a low performance cost.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_SHADOW\_BLUR** = `18`

Blurs the edges of the shadow. Can be used to hide pixel artifacts in
low resolution shadow maps. A high value can make shadows appear grainy
and can cause other unwanted artifacts. Try to keep as near default as
possible.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_TRANSMITTANCE\_BIAS** = `19`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>`
**LIGHT\_PARAM\_INTENSITY** = `20`

Constant representing the intensity of the light, measured in Lumens
when dealing with a `SpotLight3D<class_SpotLight3D>` or
`OmniLight3D<class_OmniLight3D>`, or measured in Lux with a
`DirectionalLight3D<class_DirectionalLight3D>`. Only used when
`ProjectSettings.rendering/lights_and_shadows/use_physical_light_units<class_ProjectSettings_property_rendering/lights_and_shadows/use_physical_light_units>`
is `true`.

classref-enumeration-constant

`LightParam<enum_RenderingServer_LightParam>` **LIGHT\_PARAM\_MAX** =
`21`

Represents the size of the `LightParam<enum_RenderingServer_LightParam>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightBakeMode**: `🔗<enum_RenderingServer_LightBakeMode>`

classref-enumeration-constant

`LightBakeMode<enum_RenderingServer_LightBakeMode>`
**LIGHT\_BAKE\_DISABLED** = `0`

Light is ignored when baking. This is the fastest mode, but the light
will be taken into account when baking global illumination. This mode
should generally be used for dynamic lights that change quickly, as the
effect of global illumination is less noticeable on those lights.

classref-enumeration-constant

`LightBakeMode<enum_RenderingServer_LightBakeMode>`
**LIGHT\_BAKE\_STATIC** = `1`

Light is taken into account in static baking (`VoxelGI<class_VoxelGI>`,
`LightmapGI<class_LightmapGI>`, SDFGI
(`Environment.sdfgi_enabled<class_Environment_property_sdfgi_enabled>`)).
The light can be moved around or modified, but its global illumination
will not update in real-time. This is suitable for subtle changes (such
as flickering torches), but generally not large changes such as toggling
a light on and off.

classref-enumeration-constant

`LightBakeMode<enum_RenderingServer_LightBakeMode>`
**LIGHT\_BAKE\_DYNAMIC** = `2`

Light is taken into account in dynamic baking (`VoxelGI<class_VoxelGI>`
and SDFGI
(`Environment.sdfgi_enabled<class_Environment_property_sdfgi_enabled>`)
only). The light can be moved around or modified with global
illumination updating in real-time. The light's global illumination
appearance will be slightly different compared to
`LIGHT_BAKE_STATIC<class_RenderingServer_constant_LIGHT_BAKE_STATIC>`.
This has a greater performance cost compared to
`LIGHT_BAKE_STATIC<class_RenderingServer_constant_LIGHT_BAKE_STATIC>`.
When using SDFGI, the update speed of dynamic lights is affected by
`ProjectSettings.rendering/global_illumination/sdfgi/frames_to_update_lights<class_ProjectSettings_property_rendering/global_illumination/sdfgi/frames_to_update_lights>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightOmniShadowMode**:
`🔗<enum_RenderingServer_LightOmniShadowMode>`

classref-enumeration-constant

`LightOmniShadowMode<enum_RenderingServer_LightOmniShadowMode>`
**LIGHT\_OMNI\_SHADOW\_DUAL\_PARABOLOID** = `0`

Use a dual paraboloid shadow map for omni lights.

classref-enumeration-constant

`LightOmniShadowMode<enum_RenderingServer_LightOmniShadowMode>`
**LIGHT\_OMNI\_SHADOW\_CUBE** = `1`

Use a cubemap shadow map for omni lights. Slower but better quality than
dual paraboloid.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightDirectionalShadowMode**:
`🔗<enum_RenderingServer_LightDirectionalShadowMode>`

classref-enumeration-constant

`LightDirectionalShadowMode<enum_RenderingServer_LightDirectionalShadowMode>`
**LIGHT\_DIRECTIONAL\_SHADOW\_ORTHOGONAL** = `0`

Use orthogonal shadow projection for directional light.

classref-enumeration-constant

`LightDirectionalShadowMode<enum_RenderingServer_LightDirectionalShadowMode>`
**LIGHT\_DIRECTIONAL\_SHADOW\_PARALLEL\_2\_SPLITS** = `1`

Use 2 splits for shadow projection when using directional light.

classref-enumeration-constant

`LightDirectionalShadowMode<enum_RenderingServer_LightDirectionalShadowMode>`
**LIGHT\_DIRECTIONAL\_SHADOW\_PARALLEL\_4\_SPLITS** = `2`

Use 4 splits for shadow projection when using directional light.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightDirectionalSkyMode**:
`🔗<enum_RenderingServer_LightDirectionalSkyMode>`

classref-enumeration-constant

`LightDirectionalSkyMode<enum_RenderingServer_LightDirectionalSkyMode>`
**LIGHT\_DIRECTIONAL\_SKY\_MODE\_LIGHT\_AND\_SKY** = `0`

Use DirectionalLight3D in both sky rendering and scene lighting.

classref-enumeration-constant

`LightDirectionalSkyMode<enum_RenderingServer_LightDirectionalSkyMode>`
**LIGHT\_DIRECTIONAL\_SKY\_MODE\_LIGHT\_ONLY** = `1`

Only use DirectionalLight3D in scene lighting.

classref-enumeration-constant

`LightDirectionalSkyMode<enum_RenderingServer_LightDirectionalSkyMode>`
**LIGHT\_DIRECTIONAL\_SKY\_MODE\_SKY\_ONLY** = `2`

Only use DirectionalLight3D in sky rendering.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ShadowQuality**: `🔗<enum_RenderingServer_ShadowQuality>`

classref-enumeration-constant

`ShadowQuality<enum_RenderingServer_ShadowQuality>`
**SHADOW\_QUALITY\_HARD** = `0`

Lowest shadow filtering quality (fastest). Soft shadows are not
available with this quality setting, which means the
`Light3D.shadow_blur<class_Light3D_property_shadow_blur>` property is
ignored if `Light3D.light_size<class_Light3D_property_light_size>` and
`Light3D.light_angular_distance<class_Light3D_property_light_angular_distance>`
is `0.0`.

\*\*Note:\*\* The variable shadow blur performed by
`Light3D.light_size<class_Light3D_property_light_size>` and
`Light3D.light_angular_distance<class_Light3D_property_light_angular_distance>`
is still effective when using hard shadow filtering. In this case,
`Light3D.shadow_blur<class_Light3D_property_shadow_blur>` *is* taken
into account. However, the results will not be blurred, instead the blur
amount is treated as a maximum radius for the penumbra.

classref-enumeration-constant

`ShadowQuality<enum_RenderingServer_ShadowQuality>`
**SHADOW\_QUALITY\_SOFT\_VERY\_LOW** = `1`

Very low shadow filtering quality (faster). When using this quality
setting, `Light3D.shadow_blur<class_Light3D_property_shadow_blur>` is
automatically multiplied by 0.75× to avoid introducing too much noise.
This division only applies to lights whose
`Light3D.light_size<class_Light3D_property_light_size>` or
`Light3D.light_angular_distance<class_Light3D_property_light_angular_distance>`
is `0.0`).

classref-enumeration-constant

`ShadowQuality<enum_RenderingServer_ShadowQuality>`
**SHADOW\_QUALITY\_SOFT\_LOW** = `2`

Low shadow filtering quality (fast).

classref-enumeration-constant

`ShadowQuality<enum_RenderingServer_ShadowQuality>`
**SHADOW\_QUALITY\_SOFT\_MEDIUM** = `3`

Medium low shadow filtering quality (average).

classref-enumeration-constant

`ShadowQuality<enum_RenderingServer_ShadowQuality>`
**SHADOW\_QUALITY\_SOFT\_HIGH** = `4`

High low shadow filtering quality (slow). When using this quality
setting, `Light3D.shadow_blur<class_Light3D_property_shadow_blur>` is
automatically multiplied by 1.5× to better make use of the high sample
count. This increased blur also improves the stability of dynamic object
shadows. This multiplier only applies to lights whose
`Light3D.light_size<class_Light3D_property_light_size>` or
`Light3D.light_angular_distance<class_Light3D_property_light_angular_distance>`
is `0.0`).

classref-enumeration-constant

`ShadowQuality<enum_RenderingServer_ShadowQuality>`
**SHADOW\_QUALITY\_SOFT\_ULTRA** = `5`

Highest low shadow filtering quality (slowest). When using this quality
setting, `Light3D.shadow_blur<class_Light3D_property_shadow_blur>` is
automatically multiplied by 2× to better make use of the high sample
count. This increased blur also improves the stability of dynamic object
shadows. This multiplier only applies to lights whose
`Light3D.light_size<class_Light3D_property_light_size>` or
`Light3D.light_angular_distance<class_Light3D_property_light_angular_distance>`
is `0.0`).

classref-enumeration-constant

`ShadowQuality<enum_RenderingServer_ShadowQuality>`
**SHADOW\_QUALITY\_MAX** = `6`

Represents the size of the
`ShadowQuality<enum_RenderingServer_ShadowQuality>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ReflectionProbeUpdateMode**:
`🔗<enum_RenderingServer_ReflectionProbeUpdateMode>`

classref-enumeration-constant

`ReflectionProbeUpdateMode<enum_RenderingServer_ReflectionProbeUpdateMode>`
**REFLECTION\_PROBE\_UPDATE\_ONCE** = `0`

Reflection probe will update reflections once and then stop.

classref-enumeration-constant

`ReflectionProbeUpdateMode<enum_RenderingServer_ReflectionProbeUpdateMode>`
**REFLECTION\_PROBE\_UPDATE\_ALWAYS** = `1`

Reflection probe will update each frame. This mode is necessary to
capture moving objects.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ReflectionProbeAmbientMode**:
`🔗<enum_RenderingServer_ReflectionProbeAmbientMode>`

classref-enumeration-constant

`ReflectionProbeAmbientMode<enum_RenderingServer_ReflectionProbeAmbientMode>`
**REFLECTION\_PROBE\_AMBIENT\_DISABLED** = `0`

Do not apply any ambient lighting inside the reflection probe's box
defined by its size.

classref-enumeration-constant

`ReflectionProbeAmbientMode<enum_RenderingServer_ReflectionProbeAmbientMode>`
**REFLECTION\_PROBE\_AMBIENT\_ENVIRONMENT** = `1`

Apply automatically-sourced environment lighting inside the reflection
probe's box defined by its size.

classref-enumeration-constant

`ReflectionProbeAmbientMode<enum_RenderingServer_ReflectionProbeAmbientMode>`
**REFLECTION\_PROBE\_AMBIENT\_COLOR** = `2`

Apply custom ambient lighting inside the reflection probe's box defined
by its size. See
`reflection_probe_set_ambient_color<class_RenderingServer_method_reflection_probe_set_ambient_color>`
and
`reflection_probe_set_ambient_energy<class_RenderingServer_method_reflection_probe_set_ambient_energy>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DecalTexture**: `🔗<enum_RenderingServer_DecalTexture>`

classref-enumeration-constant

`DecalTexture<enum_RenderingServer_DecalTexture>`
**DECAL\_TEXTURE\_ALBEDO** = `0`

Albedo texture slot in a decal
(`Decal.texture_albedo<class_Decal_property_texture_albedo>`).

classref-enumeration-constant

`DecalTexture<enum_RenderingServer_DecalTexture>`
**DECAL\_TEXTURE\_NORMAL** = `1`

Normal map texture slot in a decal
(`Decal.texture_normal<class_Decal_property_texture_normal>`).

classref-enumeration-constant

`DecalTexture<enum_RenderingServer_DecalTexture>`
**DECAL\_TEXTURE\_ORM** = `2`

Occlusion/Roughness/Metallic texture slot in a decal
(`Decal.texture_orm<class_Decal_property_texture_orm>`).

classref-enumeration-constant

`DecalTexture<enum_RenderingServer_DecalTexture>`
**DECAL\_TEXTURE\_EMISSION** = `3`

Emission texture slot in a decal
(`Decal.texture_emission<class_Decal_property_texture_emission>`).

classref-enumeration-constant

`DecalTexture<enum_RenderingServer_DecalTexture>`
**DECAL\_TEXTURE\_MAX** = `4`

Represents the size of the
`DecalTexture<enum_RenderingServer_DecalTexture>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DecalFilter**: `🔗<enum_RenderingServer_DecalFilter>`

classref-enumeration-constant

`DecalFilter<enum_RenderingServer_DecalFilter>`
**DECAL\_FILTER\_NEAREST** = `0`

Nearest-neighbor filter for decals (use for pixel art decals). No
mipmaps are used for rendering, which means decals at a distance will
look sharp but grainy. This has roughly the same performance cost as
using mipmaps.

classref-enumeration-constant

`DecalFilter<enum_RenderingServer_DecalFilter>`
**DECAL\_FILTER\_LINEAR** = `1`

Linear filter for decals (use for non-pixel art decals). No mipmaps are
used for rendering, which means decals at a distance will look smooth
but blurry. This has roughly the same performance cost as using mipmaps.

classref-enumeration-constant

`DecalFilter<enum_RenderingServer_DecalFilter>`
**DECAL\_FILTER\_NEAREST\_MIPMAPS** = `2`

Nearest-neighbor filter for decals (use for pixel art decals). Isotropic
mipmaps are used for rendering, which means decals at a distance will
look smooth but blurry. This has roughly the same performance cost as
not using mipmaps.

classref-enumeration-constant

`DecalFilter<enum_RenderingServer_DecalFilter>`
**DECAL\_FILTER\_LINEAR\_MIPMAPS** = `3`

Linear filter for decals (use for non-pixel art decals). Isotropic
mipmaps are used for rendering, which means decals at a distance will
look smooth but blurry. This has roughly the same performance cost as
not using mipmaps.

classref-enumeration-constant

`DecalFilter<enum_RenderingServer_DecalFilter>`
**DECAL\_FILTER\_NEAREST\_MIPMAPS\_ANISOTROPIC** = `4`

Nearest-neighbor filter for decals (use for pixel art decals).
Anisotropic mipmaps are used for rendering, which means decals at a
distance will look smooth and sharp when viewed from oblique angles.
This looks better compared to isotropic mipmaps, but is slower. The
level of anisotropic filtering is defined by
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

classref-enumeration-constant

`DecalFilter<enum_RenderingServer_DecalFilter>`
**DECAL\_FILTER\_LINEAR\_MIPMAPS\_ANISOTROPIC** = `5`

Linear filter for decals (use for non-pixel art decals). Anisotropic
mipmaps are used for rendering, which means decals at a distance will
look smooth and sharp when viewed from oblique angles. This looks better
compared to isotropic mipmaps, but is slower. The level of anisotropic
filtering is defined by
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VoxelGIQuality**: `🔗<enum_RenderingServer_VoxelGIQuality>`

classref-enumeration-constant

`VoxelGIQuality<enum_RenderingServer_VoxelGIQuality>`
**VOXEL\_GI\_QUALITY\_LOW** = `0`

Low `VoxelGI<class_VoxelGI>` rendering quality using 4 cones.

classref-enumeration-constant

`VoxelGIQuality<enum_RenderingServer_VoxelGIQuality>`
**VOXEL\_GI\_QUALITY\_HIGH** = `1`

High `VoxelGI<class_VoxelGI>` rendering quality using 6 cones.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ParticlesMode**: `🔗<enum_RenderingServer_ParticlesMode>`

classref-enumeration-constant

`ParticlesMode<enum_RenderingServer_ParticlesMode>`
**PARTICLES\_MODE\_2D** = `0`

2D particles.

classref-enumeration-constant

`ParticlesMode<enum_RenderingServer_ParticlesMode>`
**PARTICLES\_MODE\_3D** = `1`

3D particles.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ParticlesTransformAlign**:
`🔗<enum_RenderingServer_ParticlesTransformAlign>`

classref-enumeration-constant

`ParticlesTransformAlign<enum_RenderingServer_ParticlesTransformAlign>`
**PARTICLES\_TRANSFORM\_ALIGN\_DISABLED** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesTransformAlign<enum_RenderingServer_ParticlesTransformAlign>`
**PARTICLES\_TRANSFORM\_ALIGN\_Z\_BILLBOARD** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesTransformAlign<enum_RenderingServer_ParticlesTransformAlign>`
**PARTICLES\_TRANSFORM\_ALIGN\_Y\_TO\_VELOCITY** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesTransformAlign<enum_RenderingServer_ParticlesTransformAlign>`
**PARTICLES\_TRANSFORM\_ALIGN\_Z\_BILLBOARD\_Y\_TO\_VELOCITY** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ParticlesDrawOrder**:
`🔗<enum_RenderingServer_ParticlesDrawOrder>`

classref-enumeration-constant

`ParticlesDrawOrder<enum_RenderingServer_ParticlesDrawOrder>`
**PARTICLES\_DRAW\_ORDER\_INDEX** = `0`

Draw particles in the order that they appear in the particles array.

classref-enumeration-constant

`ParticlesDrawOrder<enum_RenderingServer_ParticlesDrawOrder>`
**PARTICLES\_DRAW\_ORDER\_LIFETIME** = `1`

Sort particles based on their lifetime. In other words, the particle
with the highest lifetime is drawn at the front.

classref-enumeration-constant

`ParticlesDrawOrder<enum_RenderingServer_ParticlesDrawOrder>`
**PARTICLES\_DRAW\_ORDER\_REVERSE\_LIFETIME** = `2`

Sort particles based on the inverse of their lifetime. In other words,
the particle with the lowest lifetime is drawn at the front.

classref-enumeration-constant

`ParticlesDrawOrder<enum_RenderingServer_ParticlesDrawOrder>`
**PARTICLES\_DRAW\_ORDER\_VIEW\_DEPTH** = `3`

Sort particles based on their distance to the camera.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ParticlesCollisionType**:
`🔗<enum_RenderingServer_ParticlesCollisionType>`

classref-enumeration-constant

`ParticlesCollisionType<enum_RenderingServer_ParticlesCollisionType>`
**PARTICLES\_COLLISION\_TYPE\_SPHERE\_ATTRACT** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionType<enum_RenderingServer_ParticlesCollisionType>`
**PARTICLES\_COLLISION\_TYPE\_BOX\_ATTRACT** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionType<enum_RenderingServer_ParticlesCollisionType>`
**PARTICLES\_COLLISION\_TYPE\_VECTOR\_FIELD\_ATTRACT** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionType<enum_RenderingServer_ParticlesCollisionType>`
**PARTICLES\_COLLISION\_TYPE\_SPHERE\_COLLIDE** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionType<enum_RenderingServer_ParticlesCollisionType>`
**PARTICLES\_COLLISION\_TYPE\_BOX\_COLLIDE** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionType<enum_RenderingServer_ParticlesCollisionType>`
**PARTICLES\_COLLISION\_TYPE\_SDF\_COLLIDE** = `5`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionType<enum_RenderingServer_ParticlesCollisionType>`
**PARTICLES\_COLLISION\_TYPE\_HEIGHTFIELD\_COLLIDE** = `6`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ParticlesCollisionHeightfieldResolution**:
`🔗<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`

classref-enumeration-constant

`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`
**PARTICLES\_COLLISION\_HEIGHTFIELD\_RESOLUTION\_256** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`
**PARTICLES\_COLLISION\_HEIGHTFIELD\_RESOLUTION\_512** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`
**PARTICLES\_COLLISION\_HEIGHTFIELD\_RESOLUTION\_1024** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`
**PARTICLES\_COLLISION\_HEIGHTFIELD\_RESOLUTION\_2048** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`
**PARTICLES\_COLLISION\_HEIGHTFIELD\_RESOLUTION\_4096** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`
**PARTICLES\_COLLISION\_HEIGHTFIELD\_RESOLUTION\_8192** = `5`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`
**PARTICLES\_COLLISION\_HEIGHTFIELD\_RESOLUTION\_MAX** = `6`

Represents the size of the
`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FogVolumeShape**: `🔗<enum_RenderingServer_FogVolumeShape>`

classref-enumeration-constant

`FogVolumeShape<enum_RenderingServer_FogVolumeShape>`
**FOG\_VOLUME\_SHAPE\_ELLIPSOID** = `0`

`FogVolume<class_FogVolume>` will be shaped like an ellipsoid (stretched
sphere).

classref-enumeration-constant

`FogVolumeShape<enum_RenderingServer_FogVolumeShape>`
**FOG\_VOLUME\_SHAPE\_CONE** = `1`

`FogVolume<class_FogVolume>` will be shaped like a cone pointing upwards
(in local coordinates). The cone's angle is set automatically to fill
the size. The cone will be adjusted to fit within the size. Rotate the
`FogVolume<class_FogVolume>` node to reorient the cone. Non-uniform
scaling via size is not supported (scale the
`FogVolume<class_FogVolume>` node instead).

classref-enumeration-constant

`FogVolumeShape<enum_RenderingServer_FogVolumeShape>`
**FOG\_VOLUME\_SHAPE\_CYLINDER** = `2`

`FogVolume<class_FogVolume>` will be shaped like an upright cylinder (in
local coordinates). Rotate the `FogVolume<class_FogVolume>` node to
reorient the cylinder. The cylinder will be adjusted to fit within the
size. Non-uniform scaling via size is not supported (scale the
`FogVolume<class_FogVolume>` node instead).

classref-enumeration-constant

`FogVolumeShape<enum_RenderingServer_FogVolumeShape>`
**FOG\_VOLUME\_SHAPE\_BOX** = `3`

`FogVolume<class_FogVolume>` will be shaped like a box.

classref-enumeration-constant

`FogVolumeShape<enum_RenderingServer_FogVolumeShape>`
**FOG\_VOLUME\_SHAPE\_WORLD** = `4`

`FogVolume<class_FogVolume>` will have no shape, will cover the whole
world and will not be culled.

classref-enumeration-constant

`FogVolumeShape<enum_RenderingServer_FogVolumeShape>`
**FOG\_VOLUME\_SHAPE\_MAX** = `5`

Represents the size of the
`FogVolumeShape<enum_RenderingServer_FogVolumeShape>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportScaling3DMode**:
`🔗<enum_RenderingServer_ViewportScaling3DMode>`

classref-enumeration-constant

`ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`
**VIEWPORT\_SCALING\_3D\_MODE\_BILINEAR** = `0`

Use bilinear scaling for the viewport's 3D buffer. The amount of scaling
can be set using
`Viewport.scaling_3d_scale<class_Viewport_property_scaling_3d_scale>`.
Values less than `1.0` will result in undersampling while values greater
than `1.0` will result in supersampling. A value of `1.0` disables
scaling.

classref-enumeration-constant

`ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`
**VIEWPORT\_SCALING\_3D\_MODE\_FSR** = `1`

Use AMD FidelityFX Super Resolution 1.0 upscaling for the viewport's 3D
buffer. The amount of scaling can be set using
`Viewport.scaling_3d_scale<class_Viewport_property_scaling_3d_scale>`.
Values less than `1.0` will be result in the viewport being upscaled
using FSR. Values greater than `1.0` are not supported and bilinear
downsampling will be used instead. A value of `1.0` disables scaling.

classref-enumeration-constant

`ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`
**VIEWPORT\_SCALING\_3D\_MODE\_FSR2** = `2`

Use AMD FidelityFX Super Resolution 2.2 upscaling for the viewport's 3D
buffer. The amount of scaling can be set using
`Viewport.scaling_3d_scale<class_Viewport_property_scaling_3d_scale>`.
Values less than `1.0` will be result in the viewport being upscaled
using FSR2. Values greater than `1.0` are not supported and bilinear
downsampling will be used instead. A value of `1.0` will use FSR2 at
native resolution as a TAA solution.

classref-enumeration-constant

`ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`
**VIEWPORT\_SCALING\_3D\_MODE\_MAX** = `3`

Represents the size of the
`ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportUpdateMode**:
`🔗<enum_RenderingServer_ViewportUpdateMode>`

classref-enumeration-constant

`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>`
**VIEWPORT\_UPDATE\_DISABLED** = `0`

Do not update the viewport's render target.

classref-enumeration-constant

`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>`
**VIEWPORT\_UPDATE\_ONCE** = `1`

Update the viewport's render target once, then switch to
`VIEWPORT_UPDATE_DISABLED<class_RenderingServer_constant_VIEWPORT_UPDATE_DISABLED>`.

classref-enumeration-constant

`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>`
**VIEWPORT\_UPDATE\_WHEN\_VISIBLE** = `2`

Update the viewport's render target only when it is visible. This is the
default value.

classref-enumeration-constant

`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>`
**VIEWPORT\_UPDATE\_WHEN\_PARENT\_VISIBLE** = `3`

Update the viewport's render target only when its parent is visible.

classref-enumeration-constant

`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>`
**VIEWPORT\_UPDATE\_ALWAYS** = `4`

Always update the viewport's render target.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportClearMode**: `🔗<enum_RenderingServer_ViewportClearMode>`

classref-enumeration-constant

`ViewportClearMode<enum_RenderingServer_ViewportClearMode>`
**VIEWPORT\_CLEAR\_ALWAYS** = `0`

Always clear the viewport's render target before drawing.

classref-enumeration-constant

`ViewportClearMode<enum_RenderingServer_ViewportClearMode>`
**VIEWPORT\_CLEAR\_NEVER** = `1`

Never clear the viewport's render target.

classref-enumeration-constant

`ViewportClearMode<enum_RenderingServer_ViewportClearMode>`
**VIEWPORT\_CLEAR\_ONLY\_NEXT\_FRAME** = `2`

Clear the viewport's render target on the next frame, then switch to
`VIEWPORT_CLEAR_NEVER<class_RenderingServer_constant_VIEWPORT_CLEAR_NEVER>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportEnvironmentMode**:
`🔗<enum_RenderingServer_ViewportEnvironmentMode>`

classref-enumeration-constant

`ViewportEnvironmentMode<enum_RenderingServer_ViewportEnvironmentMode>`
**VIEWPORT\_ENVIRONMENT\_DISABLED** = `0`

Disable rendering of 3D environment over 2D canvas.

classref-enumeration-constant

`ViewportEnvironmentMode<enum_RenderingServer_ViewportEnvironmentMode>`
**VIEWPORT\_ENVIRONMENT\_ENABLED** = `1`

Enable rendering of 3D environment over 2D canvas.

classref-enumeration-constant

`ViewportEnvironmentMode<enum_RenderingServer_ViewportEnvironmentMode>`
**VIEWPORT\_ENVIRONMENT\_INHERIT** = `2`

Inherit enable/disable value from parent. If the topmost parent is also
set to
`VIEWPORT_ENVIRONMENT_INHERIT<class_RenderingServer_constant_VIEWPORT_ENVIRONMENT_INHERIT>`,
then this has the same behavior as
`VIEWPORT_ENVIRONMENT_ENABLED<class_RenderingServer_constant_VIEWPORT_ENVIRONMENT_ENABLED>`.

classref-enumeration-constant

`ViewportEnvironmentMode<enum_RenderingServer_ViewportEnvironmentMode>`
**VIEWPORT\_ENVIRONMENT\_MAX** = `3`

Represents the size of the
`ViewportEnvironmentMode<enum_RenderingServer_ViewportEnvironmentMode>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportSDFOversize**:
`🔗<enum_RenderingServer_ViewportSDFOversize>`

classref-enumeration-constant

`ViewportSDFOversize<enum_RenderingServer_ViewportSDFOversize>`
**VIEWPORT\_SDF\_OVERSIZE\_100\_PERCENT** = `0`

Do not oversize the 2D signed distance field. Occluders may disappear
when touching the viewport's edges, and
`GPUParticles3D<class_GPUParticles3D>` collision may stop working
earlier than intended. This has the lowest GPU requirements.

classref-enumeration-constant

`ViewportSDFOversize<enum_RenderingServer_ViewportSDFOversize>`
**VIEWPORT\_SDF\_OVERSIZE\_120\_PERCENT** = `1`

2D signed distance field covers 20% of the viewport's size outside the
viewport on each side (top, right, bottom, left).

classref-enumeration-constant

`ViewportSDFOversize<enum_RenderingServer_ViewportSDFOversize>`
**VIEWPORT\_SDF\_OVERSIZE\_150\_PERCENT** = `2`

2D signed distance field covers 50% of the viewport's size outside the
viewport on each side (top, right, bottom, left).

classref-enumeration-constant

`ViewportSDFOversize<enum_RenderingServer_ViewportSDFOversize>`
**VIEWPORT\_SDF\_OVERSIZE\_200\_PERCENT** = `3`

2D signed distance field covers 100% of the viewport's size outside the
viewport on each side (top, right, bottom, left). This has the highest
GPU requirements.

classref-enumeration-constant

`ViewportSDFOversize<enum_RenderingServer_ViewportSDFOversize>`
**VIEWPORT\_SDF\_OVERSIZE\_MAX** = `4`

Represents the size of the
`ViewportSDFOversize<enum_RenderingServer_ViewportSDFOversize>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportSDFScale**: `🔗<enum_RenderingServer_ViewportSDFScale>`

classref-enumeration-constant

`ViewportSDFScale<enum_RenderingServer_ViewportSDFScale>`
**VIEWPORT\_SDF\_SCALE\_100\_PERCENT** = `0`

Full resolution 2D signed distance field scale. This has the highest GPU
requirements.

classref-enumeration-constant

`ViewportSDFScale<enum_RenderingServer_ViewportSDFScale>`
**VIEWPORT\_SDF\_SCALE\_50\_PERCENT** = `1`

Half resolution 2D signed distance field scale on each axis (25% of the
viewport pixel count).

classref-enumeration-constant

`ViewportSDFScale<enum_RenderingServer_ViewportSDFScale>`
**VIEWPORT\_SDF\_SCALE\_25\_PERCENT** = `2`

Quarter resolution 2D signed distance field scale on each axis (6.25% of
the viewport pixel count). This has the lowest GPU requirements.

classref-enumeration-constant

`ViewportSDFScale<enum_RenderingServer_ViewportSDFScale>`
**VIEWPORT\_SDF\_SCALE\_MAX** = `3`

Represents the size of the
`ViewportSDFScale<enum_RenderingServer_ViewportSDFScale>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportMSAA**: `🔗<enum_RenderingServer_ViewportMSAA>`

classref-enumeration-constant

`ViewportMSAA<enum_RenderingServer_ViewportMSAA>`
**VIEWPORT\_MSAA\_DISABLED** = `0`

Multisample antialiasing for 3D is disabled. This is the default value,
and also the fastest setting.

classref-enumeration-constant

`ViewportMSAA<enum_RenderingServer_ViewportMSAA>` **VIEWPORT\_MSAA\_2X**
= `1`

Multisample antialiasing uses 2 samples per pixel for 3D. This has a
moderate impact on performance.

classref-enumeration-constant

`ViewportMSAA<enum_RenderingServer_ViewportMSAA>` **VIEWPORT\_MSAA\_4X**
= `2`

Multisample antialiasing uses 4 samples per pixel for 3D. This has a
high impact on performance.

classref-enumeration-constant

`ViewportMSAA<enum_RenderingServer_ViewportMSAA>` **VIEWPORT\_MSAA\_8X**
= `3`

Multisample antialiasing uses 8 samples per pixel for 3D. This has a
very high impact on performance. Likely unsupported on low-end and older
hardware.

classref-enumeration-constant

`ViewportMSAA<enum_RenderingServer_ViewportMSAA>`
**VIEWPORT\_MSAA\_MAX** = `4`

Represents the size of the
`ViewportMSAA<enum_RenderingServer_ViewportMSAA>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportScreenSpaceAA**:
`🔗<enum_RenderingServer_ViewportScreenSpaceAA>`

classref-enumeration-constant

`ViewportScreenSpaceAA<enum_RenderingServer_ViewportScreenSpaceAA>`
**VIEWPORT\_SCREEN\_SPACE\_AA\_DISABLED** = `0`

Do not perform any antialiasing in the full screen post-process.

classref-enumeration-constant

`ViewportScreenSpaceAA<enum_RenderingServer_ViewportScreenSpaceAA>`
**VIEWPORT\_SCREEN\_SPACE\_AA\_FXAA** = `1`

Use fast approximate antialiasing. FXAA is a popular screen-space
antialiasing method, which is fast but will make the image look blurry,
especially at lower resolutions. It can still work relatively well at
large resolutions such as 1440p and 4K.

classref-enumeration-constant

`ViewportScreenSpaceAA<enum_RenderingServer_ViewportScreenSpaceAA>`
**VIEWPORT\_SCREEN\_SPACE\_AA\_MAX** = `2`

Represents the size of the
`ViewportScreenSpaceAA<enum_RenderingServer_ViewportScreenSpaceAA>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportOcclusionCullingBuildQuality**:
`🔗<enum_RenderingServer_ViewportOcclusionCullingBuildQuality>`

classref-enumeration-constant

`ViewportOcclusionCullingBuildQuality<enum_RenderingServer_ViewportOcclusionCullingBuildQuality>`
**VIEWPORT\_OCCLUSION\_BUILD\_QUALITY\_LOW** = `0`

Low occlusion culling BVH build quality (as defined by Embree). Results
in the lowest CPU usage, but least effective culling.

classref-enumeration-constant

`ViewportOcclusionCullingBuildQuality<enum_RenderingServer_ViewportOcclusionCullingBuildQuality>`
**VIEWPORT\_OCCLUSION\_BUILD\_QUALITY\_MEDIUM** = `1`

Medium occlusion culling BVH build quality (as defined by Embree).

classref-enumeration-constant

`ViewportOcclusionCullingBuildQuality<enum_RenderingServer_ViewportOcclusionCullingBuildQuality>`
**VIEWPORT\_OCCLUSION\_BUILD\_QUALITY\_HIGH** = `2`

High occlusion culling BVH build quality (as defined by Embree). Results
in the highest CPU usage, but most effective culling.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportRenderInfo**:
`🔗<enum_RenderingServer_ViewportRenderInfo>`

classref-enumeration-constant

`ViewportRenderInfo<enum_RenderingServer_ViewportRenderInfo>`
**VIEWPORT\_RENDER\_INFO\_OBJECTS\_IN\_FRAME** = `0`

Number of objects drawn in a single frame.

classref-enumeration-constant

`ViewportRenderInfo<enum_RenderingServer_ViewportRenderInfo>`
**VIEWPORT\_RENDER\_INFO\_PRIMITIVES\_IN\_FRAME** = `1`

Number of points, lines, or triangles drawn in a single frame.

classref-enumeration-constant

`ViewportRenderInfo<enum_RenderingServer_ViewportRenderInfo>`
**VIEWPORT\_RENDER\_INFO\_DRAW\_CALLS\_IN\_FRAME** = `2`

Number of draw calls during this frame.

classref-enumeration-constant

`ViewportRenderInfo<enum_RenderingServer_ViewportRenderInfo>`
**VIEWPORT\_RENDER\_INFO\_MAX** = `3`

Represents the size of the
`ViewportRenderInfo<enum_RenderingServer_ViewportRenderInfo>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportRenderInfoType**:
`🔗<enum_RenderingServer_ViewportRenderInfoType>`

classref-enumeration-constant

`ViewportRenderInfoType<enum_RenderingServer_ViewportRenderInfoType>`
**VIEWPORT\_RENDER\_INFO\_TYPE\_VISIBLE** = `0`

Visible render pass (excluding shadows).

classref-enumeration-constant

`ViewportRenderInfoType<enum_RenderingServer_ViewportRenderInfoType>`
**VIEWPORT\_RENDER\_INFO\_TYPE\_SHADOW** = `1`

Shadow render pass. Objects will be rendered several times depending on
the number of amounts of lights with shadows and the number of
directional shadow splits.

classref-enumeration-constant

`ViewportRenderInfoType<enum_RenderingServer_ViewportRenderInfoType>`
**VIEWPORT\_RENDER\_INFO\_TYPE\_CANVAS** = `2`

Canvas item rendering. This includes all 2D rendering.

classref-enumeration-constant

`ViewportRenderInfoType<enum_RenderingServer_ViewportRenderInfoType>`
**VIEWPORT\_RENDER\_INFO\_TYPE\_MAX** = `3`

Represents the size of the
`ViewportRenderInfoType<enum_RenderingServer_ViewportRenderInfoType>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportDebugDraw**: `🔗<enum_RenderingServer_ViewportDebugDraw>`

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_DISABLED** = `0`

Debug draw is disabled. Default setting.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_UNSHADED** = `1`

Objects are displayed without light information.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_LIGHTING** = `2`

Objects are displayed with only light information.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_OVERDRAW** = `3`

Objects are displayed semi-transparent with additive blending so you can
see where they are drawing over top of one another. A higher overdraw
(represented by brighter colors) means you are wasting performance on
drawing pixels that are being hidden behind others.

\*\*Note:\*\* When using this debug draw mode, custom shaders will be
ignored. This means vertex displacement won't be visible anymore.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_WIREFRAME** = `4`

Debug draw draws objects in wireframe.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_NORMAL\_BUFFER** = `5`

Normal buffer is drawn instead of regular scene so you can see the
per-pixel normals that will be used by post-processing effects.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_VOXEL\_GI\_ALBEDO** = `6`

Objects are displayed with only the albedo value from
`VoxelGI<class_VoxelGI>`s.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_VOXEL\_GI\_LIGHTING** = `7`

Objects are displayed with only the lighting value from
`VoxelGI<class_VoxelGI>`s.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_VOXEL\_GI\_EMISSION** = `8`

Objects are displayed with only the emission color from
`VoxelGI<class_VoxelGI>`s.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_SHADOW\_ATLAS** = `9`

Draws the shadow atlas that stores shadows from
`OmniLight3D<class_OmniLight3D>`s and `SpotLight3D<class_SpotLight3D>`s
in the upper left quadrant of the `Viewport<class_Viewport>`.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_DIRECTIONAL\_SHADOW\_ATLAS** = `10`

Draws the shadow atlas that stores shadows from
`DirectionalLight3D<class_DirectionalLight3D>`s in the upper left
quadrant of the `Viewport<class_Viewport>`.

The slice of the camera frustum related to the shadow map cascade is
superimposed to visualize coverage. The color of each slice matches the
colors used for
`VIEWPORT_DEBUG_DRAW_PSSM_SPLITS<class_RenderingServer_constant_VIEWPORT_DEBUG_DRAW_PSSM_SPLITS>`.
When shadow cascades are blended the overlap is taken into account when
drawing the frustum slices.

The last cascade shows all frustum slices to illustrate the coverage of
all slices.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_SCENE\_LUMINANCE** = `11`

Draws the estimated scene luminance. This is a 1×1 texture that is
generated when autoexposure is enabled to control the scene's exposure.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_SSAO** = `12`

Draws the screen space ambient occlusion texture instead of the scene so
that you can clearly see how it is affecting objects. In order for this
display mode to work, you must have
`Environment.ssao_enabled<class_Environment_property_ssao_enabled>` set
in your `WorldEnvironment<class_WorldEnvironment>`.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_SSIL** = `13`

Draws the screen space indirect lighting texture instead of the scene so
that you can clearly see how it is affecting objects. In order for this
display mode to work, you must have
`Environment.ssil_enabled<class_Environment_property_ssil_enabled>` set
in your `WorldEnvironment<class_WorldEnvironment>`.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_PSSM\_SPLITS** = `14`

Colors each PSSM split for the
`DirectionalLight3D<class_DirectionalLight3D>`s in the scene a different
color so you can see where the splits are. In order they will be colored
red, green, blue, yellow.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_DECAL\_ATLAS** = `15`

Draws the decal atlas that stores decal textures from
`Decal<class_Decal>`s.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_SDFGI** = `16`

Draws SDFGI cascade data. This is the data structure that is used to
bounce lighting against and create reflections.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_SDFGI\_PROBES** = `17`

Draws SDFGI probe data. This is the data structure that is used to give
indirect lighting dynamic objects moving within the scene.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_GI\_BUFFER** = `18`

Draws the global illumination buffer (`VoxelGI<class_VoxelGI>` or
SDFGI).

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_DISABLE\_LOD** = `19`

Disable mesh LOD. All meshes are drawn with full detail, which can be
used to compare performance.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_CLUSTER\_OMNI\_LIGHTS** = `20`

Draws the `OmniLight3D<class_OmniLight3D>` cluster. Clustering
determines where lights are positioned in screen-space, which allows the
engine to only process these portions of the screen for lighting.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_CLUSTER\_SPOT\_LIGHTS** = `21`

Draws the `SpotLight3D<class_SpotLight3D>` cluster. Clustering
determines where lights are positioned in screen-space, which allows the
engine to only process these portions of the screen for lighting.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_CLUSTER\_DECALS** = `22`

Draws the `Decal<class_Decal>` cluster. Clustering determines where
decals are positioned in screen-space, which allows the engine to only
process these portions of the screen for decals.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_CLUSTER\_REFLECTION\_PROBES** = `23`

Draws the `ReflectionProbe<class_ReflectionProbe>` cluster. Clustering
determines where reflection probes are positioned in screen-space, which
allows the engine to only process these portions of the screen for
reflection probes.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_OCCLUDERS** = `24`

Draws the occlusion culling buffer. This low-resolution occlusion
culling buffer is rasterized on the CPU and is used to check whether
instances are occluded by other objects.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_MOTION\_VECTORS** = `25`

Draws the motion vectors buffer. This is used by temporal antialiasing
to correct for motion that occurs during gameplay.

classref-enumeration-constant

`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`
**VIEWPORT\_DEBUG\_DRAW\_INTERNAL\_BUFFER** = `26`

Internal buffer is drawn instead of regular scene so you can see the
per-pixel output that will be used by post-processing effects.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportVRSMode**: `🔗<enum_RenderingServer_ViewportVRSMode>`

classref-enumeration-constant

`ViewportVRSMode<enum_RenderingServer_ViewportVRSMode>`
**VIEWPORT\_VRS\_DISABLED** = `0`

Variable rate shading is disabled.

classref-enumeration-constant

`ViewportVRSMode<enum_RenderingServer_ViewportVRSMode>`
**VIEWPORT\_VRS\_TEXTURE** = `1`

Variable rate shading uses a texture. Note, for stereoscopic use a
texture atlas with a texture for each view.

classref-enumeration-constant

`ViewportVRSMode<enum_RenderingServer_ViewportVRSMode>`
**VIEWPORT\_VRS\_XR** = `2`

Variable rate shading texture is supplied by the primary
`XRInterface<class_XRInterface>`. Note that this may override the update
mode.

classref-enumeration-constant

`ViewportVRSMode<enum_RenderingServer_ViewportVRSMode>`
**VIEWPORT\_VRS\_MAX** = `3`

Represents the size of the
`ViewportVRSMode<enum_RenderingServer_ViewportVRSMode>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ViewportVRSUpdateMode**:
`🔗<enum_RenderingServer_ViewportVRSUpdateMode>`

classref-enumeration-constant

`ViewportVRSUpdateMode<enum_RenderingServer_ViewportVRSUpdateMode>`
**VIEWPORT\_VRS\_UPDATE\_DISABLED** = `0`

The input texture for variable rate shading will not be processed.

classref-enumeration-constant

`ViewportVRSUpdateMode<enum_RenderingServer_ViewportVRSUpdateMode>`
**VIEWPORT\_VRS\_UPDATE\_ONCE** = `1`

The input texture for variable rate shading will be processed once.

classref-enumeration-constant

`ViewportVRSUpdateMode<enum_RenderingServer_ViewportVRSUpdateMode>`
**VIEWPORT\_VRS\_UPDATE\_ALWAYS** = `2`

The input texture for variable rate shading will be processed each
frame.

classref-enumeration-constant

`ViewportVRSUpdateMode<enum_RenderingServer_ViewportVRSUpdateMode>`
**VIEWPORT\_VRS\_UPDATE\_MAX** = `3`

Represents the size of the
`ViewportVRSUpdateMode<enum_RenderingServer_ViewportVRSUpdateMode>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SkyMode**: `🔗<enum_RenderingServer_SkyMode>`

classref-enumeration-constant

`SkyMode<enum_RenderingServer_SkyMode>` **SKY\_MODE\_AUTOMATIC** = `0`

Automatically selects the appropriate process mode based on your sky
shader. If your shader uses `TIME` or `POSITION`, this will use
`SKY_MODE_REALTIME<class_RenderingServer_constant_SKY_MODE_REALTIME>`.
If your shader uses any of the `LIGHT_*` variables or any custom
uniforms, this uses
`SKY_MODE_INCREMENTAL<class_RenderingServer_constant_SKY_MODE_INCREMENTAL>`.
Otherwise, this defaults to
`SKY_MODE_QUALITY<class_RenderingServer_constant_SKY_MODE_QUALITY>`.

classref-enumeration-constant

`SkyMode<enum_RenderingServer_SkyMode>` **SKY\_MODE\_QUALITY** = `1`

Uses high quality importance sampling to process the radiance map. In
general, this results in much higher quality than
`SKY_MODE_REALTIME<class_RenderingServer_constant_SKY_MODE_REALTIME>`
but takes much longer to generate. This should not be used if you plan
on changing the sky at runtime. If you are finding that the reflection
is not blurry enough and is showing sparkles or fireflies, try
increasing
`ProjectSettings.rendering/reflections/sky_reflections/ggx_samples<class_ProjectSettings_property_rendering/reflections/sky_reflections/ggx_samples>`.

classref-enumeration-constant

`SkyMode<enum_RenderingServer_SkyMode>` **SKY\_MODE\_INCREMENTAL** = `2`

Uses the same high quality importance sampling to process the radiance
map as
`SKY_MODE_QUALITY<class_RenderingServer_constant_SKY_MODE_QUALITY>`, but
updates over several frames. The number of frames is determined by
`ProjectSettings.rendering/reflections/sky_reflections/roughness_layers<class_ProjectSettings_property_rendering/reflections/sky_reflections/roughness_layers>`.
Use this when you need highest quality radiance maps, but have a sky
that updates slowly.

classref-enumeration-constant

`SkyMode<enum_RenderingServer_SkyMode>` **SKY\_MODE\_REALTIME** = `3`

Uses the fast filtering algorithm to process the radiance map. In
general this results in lower quality, but substantially faster run
times. If you need better quality, but still need to update the sky
every frame, consider turning on
`ProjectSettings.rendering/reflections/sky_reflections/fast_filter_high_quality<class_ProjectSettings_property_rendering/reflections/sky_reflections/fast_filter_high_quality>`.

\*\*Note:\*\* The fast filtering algorithm is limited to 256×256
cubemaps, so
`sky_set_radiance_size<class_RenderingServer_method_sky_set_radiance_size>`
must be set to `256`. Otherwise, a warning is printed and the overridden
radiance size is ignored.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CompositorEffectFlags**:
`🔗<enum_RenderingServer_CompositorEffectFlags>`

classref-enumeration-constant

`CompositorEffectFlags<enum_RenderingServer_CompositorEffectFlags>`
**COMPOSITOR\_EFFECT\_FLAG\_ACCESS\_RESOLVED\_COLOR** = `1`

The rendering effect requires the color buffer to be resolved if MSAA is
enabled.

classref-enumeration-constant

`CompositorEffectFlags<enum_RenderingServer_CompositorEffectFlags>`
**COMPOSITOR\_EFFECT\_FLAG\_ACCESS\_RESOLVED\_DEPTH** = `2`

The rendering effect requires the depth buffer to be resolved if MSAA is
enabled.

classref-enumeration-constant

`CompositorEffectFlags<enum_RenderingServer_CompositorEffectFlags>`
**COMPOSITOR\_EFFECT\_FLAG\_NEEDS\_MOTION\_VECTORS** = `4`

The rendering effect requires motion vectors to be produced.

classref-enumeration-constant

`CompositorEffectFlags<enum_RenderingServer_CompositorEffectFlags>`
**COMPOSITOR\_EFFECT\_FLAG\_NEEDS\_ROUGHNESS** = `8`

The rendering effect requires normals and roughness g-buffer to be
produced (Forward+ only).

classref-enumeration-constant

`CompositorEffectFlags<enum_RenderingServer_CompositorEffectFlags>`
**COMPOSITOR\_EFFECT\_FLAG\_NEEDS\_SEPARATE\_SPECULAR** = `16`

The rendering effect requires specular data to be separated out
(Forward+ only).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CompositorEffectCallbackType**:
`🔗<enum_RenderingServer_CompositorEffectCallbackType>`

classref-enumeration-constant

`CompositorEffectCallbackType<enum_RenderingServer_CompositorEffectCallbackType>`
**COMPOSITOR\_EFFECT\_CALLBACK\_TYPE\_PRE\_OPAQUE** = `0`

The callback is called before our opaque rendering pass, but after depth
prepass (if applicable).

classref-enumeration-constant

`CompositorEffectCallbackType<enum_RenderingServer_CompositorEffectCallbackType>`
**COMPOSITOR\_EFFECT\_CALLBACK\_TYPE\_POST\_OPAQUE** = `1`

The callback is called after our opaque rendering pass, but before our
sky is rendered.

classref-enumeration-constant

`CompositorEffectCallbackType<enum_RenderingServer_CompositorEffectCallbackType>`
**COMPOSITOR\_EFFECT\_CALLBACK\_TYPE\_POST\_SKY** = `2`

The callback is called after our sky is rendered, but before our back
buffers are created (and if enabled, before subsurface scattering and/or
screen space reflections).

classref-enumeration-constant

`CompositorEffectCallbackType<enum_RenderingServer_CompositorEffectCallbackType>`
**COMPOSITOR\_EFFECT\_CALLBACK\_TYPE\_PRE\_TRANSPARENT** = `3`

The callback is called before our transparent rendering pass, but after
our sky is rendered and we've created our back buffers.

classref-enumeration-constant

`CompositorEffectCallbackType<enum_RenderingServer_CompositorEffectCallbackType>`
**COMPOSITOR\_EFFECT\_CALLBACK\_TYPE\_POST\_TRANSPARENT** = `4`

The callback is called after our transparent rendering pass, but before
any built-in post-processing effects and output to our render target.

classref-enumeration-constant

`CompositorEffectCallbackType<enum_RenderingServer_CompositorEffectCallbackType>`
**COMPOSITOR\_EFFECT\_CALLBACK\_TYPE\_ANY** = `-1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentBG**: `🔗<enum_RenderingServer_EnvironmentBG>`

classref-enumeration-constant

`EnvironmentBG<enum_RenderingServer_EnvironmentBG>`
**ENV\_BG\_CLEAR\_COLOR** = `0`

Use the clear color as background.

classref-enumeration-constant

`EnvironmentBG<enum_RenderingServer_EnvironmentBG>` **ENV\_BG\_COLOR** =
`1`

Use a specified color as the background.

classref-enumeration-constant

`EnvironmentBG<enum_RenderingServer_EnvironmentBG>` **ENV\_BG\_SKY** =
`2`

Use a sky resource for the background.

classref-enumeration-constant

`EnvironmentBG<enum_RenderingServer_EnvironmentBG>` **ENV\_BG\_CANVAS**
= `3`

Use a specified canvas layer as the background. This can be useful for
instantiating a 2D scene in a 3D world.

classref-enumeration-constant

`EnvironmentBG<enum_RenderingServer_EnvironmentBG>` **ENV\_BG\_KEEP** =
`4`

Do not clear the background, use whatever was rendered last frame as the
background.

classref-enumeration-constant

`EnvironmentBG<enum_RenderingServer_EnvironmentBG>`
**ENV\_BG\_CAMERA\_FEED** = `5`

Displays a camera feed in the background.

classref-enumeration-constant

`EnvironmentBG<enum_RenderingServer_EnvironmentBG>` **ENV\_BG\_MAX** =
`6`

Represents the size of the
`EnvironmentBG<enum_RenderingServer_EnvironmentBG>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentAmbientSource**:
`🔗<enum_RenderingServer_EnvironmentAmbientSource>`

classref-enumeration-constant

`EnvironmentAmbientSource<enum_RenderingServer_EnvironmentAmbientSource>`
**ENV\_AMBIENT\_SOURCE\_BG** = `0`

Gather ambient light from whichever source is specified as the
background.

classref-enumeration-constant

`EnvironmentAmbientSource<enum_RenderingServer_EnvironmentAmbientSource>`
**ENV\_AMBIENT\_SOURCE\_DISABLED** = `1`

Disable ambient light.

classref-enumeration-constant

`EnvironmentAmbientSource<enum_RenderingServer_EnvironmentAmbientSource>`
**ENV\_AMBIENT\_SOURCE\_COLOR** = `2`

Specify a specific `Color<class_Color>` for ambient light.

classref-enumeration-constant

`EnvironmentAmbientSource<enum_RenderingServer_EnvironmentAmbientSource>`
**ENV\_AMBIENT\_SOURCE\_SKY** = `3`

Gather ambient light from the `Sky<class_Sky>` regardless of what the
background is.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentReflectionSource**:
`🔗<enum_RenderingServer_EnvironmentReflectionSource>`

classref-enumeration-constant

`EnvironmentReflectionSource<enum_RenderingServer_EnvironmentReflectionSource>`
**ENV\_REFLECTION\_SOURCE\_BG** = `0`

Use the background for reflections.

classref-enumeration-constant

`EnvironmentReflectionSource<enum_RenderingServer_EnvironmentReflectionSource>`
**ENV\_REFLECTION\_SOURCE\_DISABLED** = `1`

Disable reflections.

classref-enumeration-constant

`EnvironmentReflectionSource<enum_RenderingServer_EnvironmentReflectionSource>`
**ENV\_REFLECTION\_SOURCE\_SKY** = `2`

Use the `Sky<class_Sky>` for reflections regardless of what the
background is.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentGlowBlendMode**:
`🔗<enum_RenderingServer_EnvironmentGlowBlendMode>`

classref-enumeration-constant

`EnvironmentGlowBlendMode<enum_RenderingServer_EnvironmentGlowBlendMode>`
**ENV\_GLOW\_BLEND\_MODE\_ADDITIVE** = `0`

Additive glow blending mode. Mostly used for particles, glows (bloom),
lens flare, bright sources.

classref-enumeration-constant

`EnvironmentGlowBlendMode<enum_RenderingServer_EnvironmentGlowBlendMode>`
**ENV\_GLOW\_BLEND\_MODE\_SCREEN** = `1`

Screen glow blending mode. Increases brightness, used frequently with
bloom.

classref-enumeration-constant

`EnvironmentGlowBlendMode<enum_RenderingServer_EnvironmentGlowBlendMode>`
**ENV\_GLOW\_BLEND\_MODE\_SOFTLIGHT** = `2`

Soft light glow blending mode. Modifies contrast, exposes shadows and
highlights (vivid bloom).

classref-enumeration-constant

`EnvironmentGlowBlendMode<enum_RenderingServer_EnvironmentGlowBlendMode>`
**ENV\_GLOW\_BLEND\_MODE\_REPLACE** = `3`

Replace glow blending mode. Replaces all pixels' color by the glow
value. This can be used to simulate a full-screen blur effect by
tweaking the glow parameters to match the original image's brightness.

classref-enumeration-constant

`EnvironmentGlowBlendMode<enum_RenderingServer_EnvironmentGlowBlendMode>`
**ENV\_GLOW\_BLEND\_MODE\_MIX** = `4`

Mixes the glow with the underlying color to avoid increasing brightness
as much while still maintaining a glow effect.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentFogMode**:
`🔗<enum_RenderingServer_EnvironmentFogMode>`

classref-enumeration-constant

`EnvironmentFogMode<enum_RenderingServer_EnvironmentFogMode>`
**ENV\_FOG\_MODE\_EXPONENTIAL** = `0`

Use a physically-based fog model defined primarily by fog density.

classref-enumeration-constant

`EnvironmentFogMode<enum_RenderingServer_EnvironmentFogMode>`
**ENV\_FOG\_MODE\_DEPTH** = `1`

Use a simple fog model defined by start and end positions and a custom
curve. While not physically accurate, this model can be useful when you
need more artistic control.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentToneMapper**:
`🔗<enum_RenderingServer_EnvironmentToneMapper>`

classref-enumeration-constant

`EnvironmentToneMapper<enum_RenderingServer_EnvironmentToneMapper>`
**ENV\_TONE\_MAPPER\_LINEAR** = `0`

Output color as they came in. This can cause bright lighting to look
blown out, with noticeable clipping in the output colors.

classref-enumeration-constant

`EnvironmentToneMapper<enum_RenderingServer_EnvironmentToneMapper>`
**ENV\_TONE\_MAPPER\_REINHARD** = `1`

Use the Reinhard tonemapper. Performs a variation on rendered pixels'
colors by this formula:
`color = color * (1 + color / (white * white)) / (1 + color)`. This
avoids clipping bright highlights, but the resulting image can look a
bit dull. When
`Environment.tonemap_white<class_Environment_property_tonemap_white>` is
left at the default value of `1.0` this is identical to
`ENV_TONE_MAPPER_LINEAR<class_RenderingServer_constant_ENV_TONE_MAPPER_LINEAR>`
while also being slightly less performant.

classref-enumeration-constant

`EnvironmentToneMapper<enum_RenderingServer_EnvironmentToneMapper>`
**ENV\_TONE\_MAPPER\_FILMIC** = `2`

Use the filmic tonemapper. This avoids clipping bright highlights, with
a resulting image that usually looks more vivid than
`ENV_TONE_MAPPER_REINHARD<class_RenderingServer_constant_ENV_TONE_MAPPER_REINHARD>`.

classref-enumeration-constant

`EnvironmentToneMapper<enum_RenderingServer_EnvironmentToneMapper>`
**ENV\_TONE\_MAPPER\_ACES** = `3`

Use the Academy Color Encoding System tonemapper. ACES is slightly more
expensive than other options, but it handles bright lighting in a more
realistic fashion by desaturating it as it becomes brighter. ACES
typically has a more contrasted output compared to
`ENV_TONE_MAPPER_REINHARD<class_RenderingServer_constant_ENV_TONE_MAPPER_REINHARD>`
and
`ENV_TONE_MAPPER_FILMIC<class_RenderingServer_constant_ENV_TONE_MAPPER_FILMIC>`.

\*\*Note:\*\* This tonemapping operator is called "ACES Fitted" in Godot
3.x.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentSSRRoughnessQuality**:
`🔗<enum_RenderingServer_EnvironmentSSRRoughnessQuality>`

classref-enumeration-constant

`EnvironmentSSRRoughnessQuality<enum_RenderingServer_EnvironmentSSRRoughnessQuality>`
**ENV\_SSR\_ROUGHNESS\_QUALITY\_DISABLED** = `0`

Lowest quality of roughness filter for screen-space reflections. Rough
materials will not have blurrier screen-space reflections compared to
smooth (non-rough) materials. This is the fastest option.

classref-enumeration-constant

`EnvironmentSSRRoughnessQuality<enum_RenderingServer_EnvironmentSSRRoughnessQuality>`
**ENV\_SSR\_ROUGHNESS\_QUALITY\_LOW** = `1`

Low quality of roughness filter for screen-space reflections.

classref-enumeration-constant

`EnvironmentSSRRoughnessQuality<enum_RenderingServer_EnvironmentSSRRoughnessQuality>`
**ENV\_SSR\_ROUGHNESS\_QUALITY\_MEDIUM** = `2`

Medium quality of roughness filter for screen-space reflections.

classref-enumeration-constant

`EnvironmentSSRRoughnessQuality<enum_RenderingServer_EnvironmentSSRRoughnessQuality>`
**ENV\_SSR\_ROUGHNESS\_QUALITY\_HIGH** = `3`

High quality of roughness filter for screen-space reflections. This is
the slowest option.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentSSAOQuality**:
`🔗<enum_RenderingServer_EnvironmentSSAOQuality>`

classref-enumeration-constant

`EnvironmentSSAOQuality<enum_RenderingServer_EnvironmentSSAOQuality>`
**ENV\_SSAO\_QUALITY\_VERY\_LOW** = `0`

Lowest quality of screen-space ambient occlusion.

classref-enumeration-constant

`EnvironmentSSAOQuality<enum_RenderingServer_EnvironmentSSAOQuality>`
**ENV\_SSAO\_QUALITY\_LOW** = `1`

Low quality screen-space ambient occlusion.

classref-enumeration-constant

`EnvironmentSSAOQuality<enum_RenderingServer_EnvironmentSSAOQuality>`
**ENV\_SSAO\_QUALITY\_MEDIUM** = `2`

Medium quality screen-space ambient occlusion.

classref-enumeration-constant

`EnvironmentSSAOQuality<enum_RenderingServer_EnvironmentSSAOQuality>`
**ENV\_SSAO\_QUALITY\_HIGH** = `3`

High quality screen-space ambient occlusion.

classref-enumeration-constant

`EnvironmentSSAOQuality<enum_RenderingServer_EnvironmentSSAOQuality>`
**ENV\_SSAO\_QUALITY\_ULTRA** = `4`

Highest quality screen-space ambient occlusion. Uses the adaptive target
setting which can be dynamically adjusted to smoothly balance
performance and visual quality.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentSSILQuality**:
`🔗<enum_RenderingServer_EnvironmentSSILQuality>`

classref-enumeration-constant

`EnvironmentSSILQuality<enum_RenderingServer_EnvironmentSSILQuality>`
**ENV\_SSIL\_QUALITY\_VERY\_LOW** = `0`

Lowest quality of screen-space indirect lighting.

classref-enumeration-constant

`EnvironmentSSILQuality<enum_RenderingServer_EnvironmentSSILQuality>`
**ENV\_SSIL\_QUALITY\_LOW** = `1`

Low quality screen-space indirect lighting.

classref-enumeration-constant

`EnvironmentSSILQuality<enum_RenderingServer_EnvironmentSSILQuality>`
**ENV\_SSIL\_QUALITY\_MEDIUM** = `2`

High quality screen-space indirect lighting.

classref-enumeration-constant

`EnvironmentSSILQuality<enum_RenderingServer_EnvironmentSSILQuality>`
**ENV\_SSIL\_QUALITY\_HIGH** = `3`

High quality screen-space indirect lighting.

classref-enumeration-constant

`EnvironmentSSILQuality<enum_RenderingServer_EnvironmentSSILQuality>`
**ENV\_SSIL\_QUALITY\_ULTRA** = `4`

Highest quality screen-space indirect lighting. Uses the adaptive target
setting which can be dynamically adjusted to smoothly balance
performance and visual quality.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentSDFGIYScale**:
`🔗<enum_RenderingServer_EnvironmentSDFGIYScale>`

classref-enumeration-constant

`EnvironmentSDFGIYScale<enum_RenderingServer_EnvironmentSDFGIYScale>`
**ENV\_SDFGI\_Y\_SCALE\_50\_PERCENT** = `0`

Use 50% scale for SDFGI on the Y (vertical) axis. SDFGI cells will be
twice as short as they are wide. This allows providing increased GI
detail and reduced light leaking with thin floors and ceilings. This is
usually the best choice for scenes that don't feature much verticality.

classref-enumeration-constant

`EnvironmentSDFGIYScale<enum_RenderingServer_EnvironmentSDFGIYScale>`
**ENV\_SDFGI\_Y\_SCALE\_75\_PERCENT** = `1`

Use 75% scale for SDFGI on the Y (vertical) axis. This is a balance
between the 50% and 100% SDFGI Y scales.

classref-enumeration-constant

`EnvironmentSDFGIYScale<enum_RenderingServer_EnvironmentSDFGIYScale>`
**ENV\_SDFGI\_Y\_SCALE\_100\_PERCENT** = `2`

Use 100% scale for SDFGI on the Y (vertical) axis. SDFGI cells will be
as tall as they are wide. This is usually the best choice for highly
vertical scenes. The downside is that light leaking may become more
noticeable with thin floors and ceilings.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentSDFGIRayCount**:
`🔗<enum_RenderingServer_EnvironmentSDFGIRayCount>`

classref-enumeration-constant

`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
**ENV\_SDFGI\_RAY\_COUNT\_4** = `0`

Throw 4 rays per frame when converging SDFGI. This has the lowest GPU
requirements, but creates the most noisy result.

classref-enumeration-constant

`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
**ENV\_SDFGI\_RAY\_COUNT\_8** = `1`

Throw 8 rays per frame when converging SDFGI.

classref-enumeration-constant

`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
**ENV\_SDFGI\_RAY\_COUNT\_16** = `2`

Throw 16 rays per frame when converging SDFGI.

classref-enumeration-constant

`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
**ENV\_SDFGI\_RAY\_COUNT\_32** = `3`

Throw 32 rays per frame when converging SDFGI.

classref-enumeration-constant

`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
**ENV\_SDFGI\_RAY\_COUNT\_64** = `4`

Throw 64 rays per frame when converging SDFGI.

classref-enumeration-constant

`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
**ENV\_SDFGI\_RAY\_COUNT\_96** = `5`

Throw 96 rays per frame when converging SDFGI. This has high GPU
requirements.

classref-enumeration-constant

`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
**ENV\_SDFGI\_RAY\_COUNT\_128** = `6`

Throw 128 rays per frame when converging SDFGI. This has very high GPU
requirements, but creates the least noisy result.

classref-enumeration-constant

`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
**ENV\_SDFGI\_RAY\_COUNT\_MAX** = `7`

Represents the size of the
`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentSDFGIFramesToConverge**:
`🔗<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`

classref-enumeration-constant

`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`
**ENV\_SDFGI\_CONVERGE\_IN\_5\_FRAMES** = `0`

Converge SDFGI over 5 frames. This is the most responsive, but creates
the most noisy result with a given ray count.

classref-enumeration-constant

`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`
**ENV\_SDFGI\_CONVERGE\_IN\_10\_FRAMES** = `1`

Configure SDFGI to fully converge over 10 frames.

classref-enumeration-constant

`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`
**ENV\_SDFGI\_CONVERGE\_IN\_15\_FRAMES** = `2`

Configure SDFGI to fully converge over 15 frames.

classref-enumeration-constant

`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`
**ENV\_SDFGI\_CONVERGE\_IN\_20\_FRAMES** = `3`

Configure SDFGI to fully converge over 20 frames.

classref-enumeration-constant

`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`
**ENV\_SDFGI\_CONVERGE\_IN\_25\_FRAMES** = `4`

Configure SDFGI to fully converge over 25 frames.

classref-enumeration-constant

`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`
**ENV\_SDFGI\_CONVERGE\_IN\_30\_FRAMES** = `5`

Configure SDFGI to fully converge over 30 frames. This is the least
responsive, but creates the least noisy result with a given ray count.

classref-enumeration-constant

`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`
**ENV\_SDFGI\_CONVERGE\_MAX** = `6`

Represents the size of the
`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentSDFGIFramesToUpdateLight**:
`🔗<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`

classref-enumeration-constant

`EnvironmentSDFGIFramesToUpdateLight<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`
**ENV\_SDFGI\_UPDATE\_LIGHT\_IN\_1\_FRAME** = `0`

Update indirect light from dynamic lights in SDFGI over 1 frame. This is
the most responsive, but has the highest GPU requirements.

classref-enumeration-constant

`EnvironmentSDFGIFramesToUpdateLight<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`
**ENV\_SDFGI\_UPDATE\_LIGHT\_IN\_2\_FRAMES** = `1`

Update indirect light from dynamic lights in SDFGI over 2 frames.

classref-enumeration-constant

`EnvironmentSDFGIFramesToUpdateLight<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`
**ENV\_SDFGI\_UPDATE\_LIGHT\_IN\_4\_FRAMES** = `2`

Update indirect light from dynamic lights in SDFGI over 4 frames.

classref-enumeration-constant

`EnvironmentSDFGIFramesToUpdateLight<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`
**ENV\_SDFGI\_UPDATE\_LIGHT\_IN\_8\_FRAMES** = `3`

Update indirect light from dynamic lights in SDFGI over 8 frames.

classref-enumeration-constant

`EnvironmentSDFGIFramesToUpdateLight<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`
**ENV\_SDFGI\_UPDATE\_LIGHT\_IN\_16\_FRAMES** = `4`

Update indirect light from dynamic lights in SDFGI over 16 frames. This
is the least responsive, but has the lowest GPU requirements.

classref-enumeration-constant

`EnvironmentSDFGIFramesToUpdateLight<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`
**ENV\_SDFGI\_UPDATE\_LIGHT\_MAX** = `5`

Represents the size of the
`EnvironmentSDFGIFramesToUpdateLight<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SubSurfaceScatteringQuality**:
`🔗<enum_RenderingServer_SubSurfaceScatteringQuality>`

classref-enumeration-constant

`SubSurfaceScatteringQuality<enum_RenderingServer_SubSurfaceScatteringQuality>`
**SUB\_SURFACE\_SCATTERING\_QUALITY\_DISABLED** = `0`

Disables subsurface scattering entirely, even on materials that have
`BaseMaterial3D.subsurf_scatter_enabled<class_BaseMaterial3D_property_subsurf_scatter_enabled>`
set to `true`. This has the lowest GPU requirements.

classref-enumeration-constant

`SubSurfaceScatteringQuality<enum_RenderingServer_SubSurfaceScatteringQuality>`
**SUB\_SURFACE\_SCATTERING\_QUALITY\_LOW** = `1`

Low subsurface scattering quality.

classref-enumeration-constant

`SubSurfaceScatteringQuality<enum_RenderingServer_SubSurfaceScatteringQuality>`
**SUB\_SURFACE\_SCATTERING\_QUALITY\_MEDIUM** = `2`

Medium subsurface scattering quality.

classref-enumeration-constant

`SubSurfaceScatteringQuality<enum_RenderingServer_SubSurfaceScatteringQuality>`
**SUB\_SURFACE\_SCATTERING\_QUALITY\_HIGH** = `3`

High subsurface scattering quality. This has the highest GPU
requirements.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DOFBokehShape**: `🔗<enum_RenderingServer_DOFBokehShape>`

classref-enumeration-constant

`DOFBokehShape<enum_RenderingServer_DOFBokehShape>` **DOF\_BOKEH\_BOX**
= `0`

Calculate the DOF blur using a box filter. The fastest option, but
results in obvious lines in blur pattern.

classref-enumeration-constant

`DOFBokehShape<enum_RenderingServer_DOFBokehShape>`
**DOF\_BOKEH\_HEXAGON** = `1`

Calculates DOF blur using a hexagon shaped filter.

classref-enumeration-constant

`DOFBokehShape<enum_RenderingServer_DOFBokehShape>`
**DOF\_BOKEH\_CIRCLE** = `2`

Calculates DOF blur using a circle shaped filter. Best quality and most
realistic, but slowest. Use only for areas where a lot of performance
can be dedicated to post-processing (e.g. cutscenes).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DOFBlurQuality**: `🔗<enum_RenderingServer_DOFBlurQuality>`

classref-enumeration-constant

`DOFBlurQuality<enum_RenderingServer_DOFBlurQuality>`
**DOF\_BLUR\_QUALITY\_VERY\_LOW** = `0`

Lowest quality DOF blur. This is the fastest setting, but you may be
able to see filtering artifacts.

classref-enumeration-constant

`DOFBlurQuality<enum_RenderingServer_DOFBlurQuality>`
**DOF\_BLUR\_QUALITY\_LOW** = `1`

Low quality DOF blur.

classref-enumeration-constant

`DOFBlurQuality<enum_RenderingServer_DOFBlurQuality>`
**DOF\_BLUR\_QUALITY\_MEDIUM** = `2`

Medium quality DOF blur.

classref-enumeration-constant

`DOFBlurQuality<enum_RenderingServer_DOFBlurQuality>`
**DOF\_BLUR\_QUALITY\_HIGH** = `3`

Highest quality DOF blur. Results in the smoothest looking blur by
taking the most samples, but is also significantly slower.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **InstanceType**: `🔗<enum_RenderingServer_InstanceType>`

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>` **INSTANCE\_NONE** =
`0`

The instance does not have a type.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>` **INSTANCE\_MESH** =
`1`

The instance is a mesh.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>`
**INSTANCE\_MULTIMESH** = `2`

The instance is a multimesh.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>`
**INSTANCE\_PARTICLES** = `3`

The instance is a particle emitter.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>`
**INSTANCE\_PARTICLES\_COLLISION** = `4`

The instance is a GPUParticles collision shape.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>` **INSTANCE\_LIGHT** =
`5`

The instance is a light.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>`
**INSTANCE\_REFLECTION\_PROBE** = `6`

The instance is a reflection probe.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>` **INSTANCE\_DECAL** =
`7`

The instance is a decal.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>`
**INSTANCE\_VOXEL\_GI** = `8`

The instance is a VoxelGI.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>` **INSTANCE\_LIGHTMAP**
= `9`

The instance is a lightmap.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>` **INSTANCE\_OCCLUDER**
= `10`

The instance is an occlusion culling occluder.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>`
**INSTANCE\_VISIBLITY\_NOTIFIER** = `11`

The instance is a visible on-screen notifier.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>`
**INSTANCE\_FOG\_VOLUME** = `12`

The instance is a fog volume.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>` **INSTANCE\_MAX** =
`13`

Represents the size of the
`InstanceType<enum_RenderingServer_InstanceType>` enum.

classref-enumeration-constant

`InstanceType<enum_RenderingServer_InstanceType>`
**INSTANCE\_GEOMETRY\_MASK** = `14`

A combination of the flags of geometry instances (mesh, multimesh,
immediate and particles).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **InstanceFlags**: `🔗<enum_RenderingServer_InstanceFlags>`

classref-enumeration-constant

`InstanceFlags<enum_RenderingServer_InstanceFlags>`
**INSTANCE\_FLAG\_USE\_BAKED\_LIGHT** = `0`

Allows the instance to be used in baked lighting.

classref-enumeration-constant

`InstanceFlags<enum_RenderingServer_InstanceFlags>`
**INSTANCE\_FLAG\_USE\_DYNAMIC\_GI** = `1`

Allows the instance to be used with dynamic global illumination.

classref-enumeration-constant

`InstanceFlags<enum_RenderingServer_InstanceFlags>`
**INSTANCE\_FLAG\_DRAW\_NEXT\_FRAME\_IF\_VISIBLE** = `2`

When set, manually requests to draw geometry on next frame.

classref-enumeration-constant

`InstanceFlags<enum_RenderingServer_InstanceFlags>`
**INSTANCE\_FLAG\_IGNORE\_OCCLUSION\_CULLING** = `3`

Always draw, even if the instance would be culled by occlusion culling.
Does not affect view frustum culling.

classref-enumeration-constant

`InstanceFlags<enum_RenderingServer_InstanceFlags>`
**INSTANCE\_FLAG\_MAX** = `4`

Represents the size of the
`InstanceFlags<enum_RenderingServer_InstanceFlags>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ShadowCastingSetting**:
`🔗<enum_RenderingServer_ShadowCastingSetting>`

classref-enumeration-constant

`ShadowCastingSetting<enum_RenderingServer_ShadowCastingSetting>`
**SHADOW\_CASTING\_SETTING\_OFF** = `0`

Disable shadows from this instance.

classref-enumeration-constant

`ShadowCastingSetting<enum_RenderingServer_ShadowCastingSetting>`
**SHADOW\_CASTING\_SETTING\_ON** = `1`

Cast shadows from this instance.

classref-enumeration-constant

`ShadowCastingSetting<enum_RenderingServer_ShadowCastingSetting>`
**SHADOW\_CASTING\_SETTING\_DOUBLE\_SIDED** = `2`

Disable backface culling when rendering the shadow of the object. This
is slightly slower but may result in more correct shadows.

classref-enumeration-constant

`ShadowCastingSetting<enum_RenderingServer_ShadowCastingSetting>`
**SHADOW\_CASTING\_SETTING\_SHADOWS\_ONLY** = `3`

Only render the shadows from the object. The object itself will not be
drawn.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VisibilityRangeFadeMode**:
`🔗<enum_RenderingServer_VisibilityRangeFadeMode>`

classref-enumeration-constant

`VisibilityRangeFadeMode<enum_RenderingServer_VisibilityRangeFadeMode>`
**VISIBILITY\_RANGE\_FADE\_DISABLED** = `0`

Disable visibility range fading for the given instance.

classref-enumeration-constant

`VisibilityRangeFadeMode<enum_RenderingServer_VisibilityRangeFadeMode>`
**VISIBILITY\_RANGE\_FADE\_SELF** = `1`

Fade-out the given instance when it approaches its visibility range
limits.

classref-enumeration-constant

`VisibilityRangeFadeMode<enum_RenderingServer_VisibilityRangeFadeMode>`
**VISIBILITY\_RANGE\_FADE\_DEPENDENCIES** = `2`

Fade-in the given instance's dependencies when reaching its visibility
range limits.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BakeChannels**: `🔗<enum_RenderingServer_BakeChannels>`

classref-enumeration-constant

`BakeChannels<enum_RenderingServer_BakeChannels>`
**BAKE\_CHANNEL\_ALBEDO\_ALPHA** = `0`

Index of `Image<class_Image>` in array of `Image<class_Image>`s returned
by `bake_render_uv2<class_RenderingServer_method_bake_render_uv2>`.
Image uses `Image.FORMAT_RGBA8<class_Image_constant_FORMAT_RGBA8>` and
contains albedo color in the `.rgb` channels and alpha in the `.a`
channel.

classref-enumeration-constant

`BakeChannels<enum_RenderingServer_BakeChannels>`
**BAKE\_CHANNEL\_NORMAL** = `1`

Index of `Image<class_Image>` in array of `Image<class_Image>`s returned
by `bake_render_uv2<class_RenderingServer_method_bake_render_uv2>`.
Image uses `Image.FORMAT_RGBA8<class_Image_constant_FORMAT_RGBA8>` and
contains the per-pixel normal of the object in the `.rgb` channels and
nothing in the `.a` channel. The per-pixel normal is encoded as
`normal * 0.5 + 0.5`.

classref-enumeration-constant

`BakeChannels<enum_RenderingServer_BakeChannels>` **BAKE\_CHANNEL\_ORM**
= `2`

Index of `Image<class_Image>` in array of `Image<class_Image>`s returned
by `bake_render_uv2<class_RenderingServer_method_bake_render_uv2>`.
Image uses `Image.FORMAT_RGBA8<class_Image_constant_FORMAT_RGBA8>` and
contains ambient occlusion (from material and decals only) in the `.r`
channel, roughness in the `.g` channel, metallic in the `.b` channel and
sub surface scattering amount in the `.a` channel.

classref-enumeration-constant

`BakeChannels<enum_RenderingServer_BakeChannels>`
**BAKE\_CHANNEL\_EMISSION** = `3`

Index of `Image<class_Image>` in array of `Image<class_Image>`s returned
by `bake_render_uv2<class_RenderingServer_method_bake_render_uv2>`.
Image uses `Image.FORMAT_RGBAH<class_Image_constant_FORMAT_RGBAH>` and
contains emission color in the `.rgb` channels and nothing in the `.a`
channel.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CanvasTextureChannel**:
`🔗<enum_RenderingServer_CanvasTextureChannel>`

classref-enumeration-constant

`CanvasTextureChannel<enum_RenderingServer_CanvasTextureChannel>`
**CANVAS\_TEXTURE\_CHANNEL\_DIFFUSE** = `0`

Diffuse canvas texture
(`CanvasTexture.diffuse_texture<class_CanvasTexture_property_diffuse_texture>`).

classref-enumeration-constant

`CanvasTextureChannel<enum_RenderingServer_CanvasTextureChannel>`
**CANVAS\_TEXTURE\_CHANNEL\_NORMAL** = `1`

Normal map canvas texture
(`CanvasTexture.normal_texture<class_CanvasTexture_property_normal_texture>`).

classref-enumeration-constant

`CanvasTextureChannel<enum_RenderingServer_CanvasTextureChannel>`
**CANVAS\_TEXTURE\_CHANNEL\_SPECULAR** = `2`

Specular map canvas texture
(`CanvasTexture.specular_texture<class_CanvasTexture_property_specular_texture>`).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **NinePatchAxisMode**: `🔗<enum_RenderingServer_NinePatchAxisMode>`

classref-enumeration-constant

`NinePatchAxisMode<enum_RenderingServer_NinePatchAxisMode>`
**NINE\_PATCH\_STRETCH** = `0`

The nine patch gets stretched where needed.

classref-enumeration-constant

`NinePatchAxisMode<enum_RenderingServer_NinePatchAxisMode>`
**NINE\_PATCH\_TILE** = `1`

The nine patch gets filled with tiles where needed.

classref-enumeration-constant

`NinePatchAxisMode<enum_RenderingServer_NinePatchAxisMode>`
**NINE\_PATCH\_TILE\_FIT** = `2`

The nine patch gets filled with tiles where needed and stretches them a
bit if needed.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CanvasItemTextureFilter**:
`🔗<enum_RenderingServer_CanvasItemTextureFilter>`

classref-enumeration-constant

`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
**CANVAS\_ITEM\_TEXTURE\_FILTER\_DEFAULT** = `0`

Uses the default filter mode for this `Viewport<class_Viewport>`.

classref-enumeration-constant

`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
**CANVAS\_ITEM\_TEXTURE\_FILTER\_NEAREST** = `1`

The texture filter reads from the nearest pixel only. This makes the
texture look pixelated from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
**CANVAS\_ITEM\_TEXTURE\_FILTER\_LINEAR** = `2`

The texture filter blends between the nearest 4 pixels. This makes the
texture look smooth from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
**CANVAS\_ITEM\_TEXTURE\_FILTER\_NEAREST\_WITH\_MIPMAPS** = `3`

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

`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
**CANVAS\_ITEM\_TEXTURE\_FILTER\_LINEAR\_WITH\_MIPMAPS** = `4`

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

`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
**CANVAS\_ITEM\_TEXTURE\_FILTER\_NEAREST\_WITH\_MIPMAPS\_ANISOTROPIC** =
`5`

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
`CANVAS_ITEM_TEXTURE_FILTER_NEAREST_WITH_MIPMAPS<class_RenderingServer_constant_CANVAS_ITEM_TEXTURE_FILTER_NEAREST_WITH_MIPMAPS>`
is usually more appropriate in this case.

classref-enumeration-constant

`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
**CANVAS\_ITEM\_TEXTURE\_FILTER\_LINEAR\_WITH\_MIPMAPS\_ANISOTROPIC** =
`6`

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
`CANVAS_ITEM_TEXTURE_FILTER_LINEAR_WITH_MIPMAPS<class_RenderingServer_constant_CANVAS_ITEM_TEXTURE_FILTER_LINEAR_WITH_MIPMAPS>`
is usually more appropriate in this case.

classref-enumeration-constant

`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
**CANVAS\_ITEM\_TEXTURE\_FILTER\_MAX** = `7`

Max value for
`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CanvasItemTextureRepeat**:
`🔗<enum_RenderingServer_CanvasItemTextureRepeat>`

classref-enumeration-constant

`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`
**CANVAS\_ITEM\_TEXTURE\_REPEAT\_DEFAULT** = `0`

Uses the default repeat mode for this `Viewport<class_Viewport>`.

classref-enumeration-constant

`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`
**CANVAS\_ITEM\_TEXTURE\_REPEAT\_DISABLED** = `1`

Disables textures repeating. Instead, when reading UVs outside the 0-1
range, the value will be clamped to the edge of the texture, resulting
in a stretched out look at the borders of the texture.

classref-enumeration-constant

`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`
**CANVAS\_ITEM\_TEXTURE\_REPEAT\_ENABLED** = `2`

Enables the texture to repeat when UV coordinates are outside the 0-1
range. If using one of the linear filtering modes, this can result in
artifacts at the edges of a texture when the sampler filters across the
edges of the texture.

classref-enumeration-constant

`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`
**CANVAS\_ITEM\_TEXTURE\_REPEAT\_MIRROR** = `3`

Flip the texture when repeating so that the edge lines up instead of
abruptly changing.

classref-enumeration-constant

`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`
**CANVAS\_ITEM\_TEXTURE\_REPEAT\_MAX** = `4`

Max value for
`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CanvasGroupMode**: `🔗<enum_RenderingServer_CanvasGroupMode>`

classref-enumeration-constant

`CanvasGroupMode<enum_RenderingServer_CanvasGroupMode>`
**CANVAS\_GROUP\_MODE\_DISABLED** = `0`

Child draws over parent and is not clipped.

classref-enumeration-constant

`CanvasGroupMode<enum_RenderingServer_CanvasGroupMode>`
**CANVAS\_GROUP\_MODE\_CLIP\_ONLY** = `1`

Parent is used for the purposes of clipping only. Child is clipped to
the parent's visible area, parent is not drawn.

classref-enumeration-constant

`CanvasGroupMode<enum_RenderingServer_CanvasGroupMode>`
**CANVAS\_GROUP\_MODE\_CLIP\_AND\_DRAW** = `2`

Parent is used for clipping child, but parent is also drawn underneath
child as normal before clipping child to its visible area.

classref-enumeration-constant

`CanvasGroupMode<enum_RenderingServer_CanvasGroupMode>`
**CANVAS\_GROUP\_MODE\_TRANSPARENT** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CanvasLightMode**: `🔗<enum_RenderingServer_CanvasLightMode>`

classref-enumeration-constant

`CanvasLightMode<enum_RenderingServer_CanvasLightMode>`
**CANVAS\_LIGHT\_MODE\_POINT** = `0`

2D point light (see `PointLight2D<class_PointLight2D>`).

classref-enumeration-constant

`CanvasLightMode<enum_RenderingServer_CanvasLightMode>`
**CANVAS\_LIGHT\_MODE\_DIRECTIONAL** = `1`

2D directional (sun/moon) light (see
`DirectionalLight2D<class_DirectionalLight2D>`).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CanvasLightBlendMode**:
`🔗<enum_RenderingServer_CanvasLightBlendMode>`

classref-enumeration-constant

`CanvasLightBlendMode<enum_RenderingServer_CanvasLightBlendMode>`
**CANVAS\_LIGHT\_BLEND\_MODE\_ADD** = `0`

Adds light color additive to the canvas.

classref-enumeration-constant

`CanvasLightBlendMode<enum_RenderingServer_CanvasLightBlendMode>`
**CANVAS\_LIGHT\_BLEND\_MODE\_SUB** = `1`

Adds light color subtractive to the canvas.

classref-enumeration-constant

`CanvasLightBlendMode<enum_RenderingServer_CanvasLightBlendMode>`
**CANVAS\_LIGHT\_BLEND\_MODE\_MIX** = `2`

The light adds color depending on transparency.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CanvasLightShadowFilter**:
`🔗<enum_RenderingServer_CanvasLightShadowFilter>`

classref-enumeration-constant

`CanvasLightShadowFilter<enum_RenderingServer_CanvasLightShadowFilter>`
**CANVAS\_LIGHT\_FILTER\_NONE** = `0`

Do not apply a filter to canvas light shadows.

classref-enumeration-constant

`CanvasLightShadowFilter<enum_RenderingServer_CanvasLightShadowFilter>`
**CANVAS\_LIGHT\_FILTER\_PCF5** = `1`

Use PCF5 filtering to filter canvas light shadows.

classref-enumeration-constant

`CanvasLightShadowFilter<enum_RenderingServer_CanvasLightShadowFilter>`
**CANVAS\_LIGHT\_FILTER\_PCF13** = `2`

Use PCF13 filtering to filter canvas light shadows.

classref-enumeration-constant

`CanvasLightShadowFilter<enum_RenderingServer_CanvasLightShadowFilter>`
**CANVAS\_LIGHT\_FILTER\_MAX** = `3`

Max value of the
`CanvasLightShadowFilter<enum_RenderingServer_CanvasLightShadowFilter>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CanvasOccluderPolygonCullMode**:
`🔗<enum_RenderingServer_CanvasOccluderPolygonCullMode>`

classref-enumeration-constant

`CanvasOccluderPolygonCullMode<enum_RenderingServer_CanvasOccluderPolygonCullMode>`
**CANVAS\_OCCLUDER\_POLYGON\_CULL\_DISABLED** = `0`

Culling of the canvas occluder is disabled.

classref-enumeration-constant

`CanvasOccluderPolygonCullMode<enum_RenderingServer_CanvasOccluderPolygonCullMode>`
**CANVAS\_OCCLUDER\_POLYGON\_CULL\_CLOCKWISE** = `1`

Culling of the canvas occluder is clockwise.

classref-enumeration-constant

`CanvasOccluderPolygonCullMode<enum_RenderingServer_CanvasOccluderPolygonCullMode>`
**CANVAS\_OCCLUDER\_POLYGON\_CULL\_COUNTER\_CLOCKWISE** = `2`

Culling of the canvas occluder is counterclockwise.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **GlobalShaderParameterType**:
`🔗<enum_RenderingServer_GlobalShaderParameterType>`

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_BOOL** = `0`

Boolean global shader parameter (`global uniform bool ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_BVEC2** = `1`

2-dimensional boolean vector global shader parameter
(`global uniform bvec2 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_BVEC3** = `2`

3-dimensional boolean vector global shader parameter
(`global uniform bvec3 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_BVEC4** = `3`

4-dimensional boolean vector global shader parameter
(`global uniform bvec4 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_INT** = `4`

Integer global shader parameter (`global uniform int ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_IVEC2** = `5`

2-dimensional integer vector global shader parameter
(`global uniform ivec2 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_IVEC3** = `6`

3-dimensional integer vector global shader parameter
(`global uniform ivec3 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_IVEC4** = `7`

4-dimensional integer vector global shader parameter
(`global uniform ivec4 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_RECT2I** = `8`

2-dimensional integer rectangle global shader parameter
(`global uniform ivec4 ...`). Equivalent to
`GLOBAL_VAR_TYPE_IVEC4<class_RenderingServer_constant_GLOBAL_VAR_TYPE_IVEC4>`
in shader code, but exposed as a `Rect2i<class_Rect2i>` in the editor
UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_UINT** = `9`

Unsigned integer global shader parameter (`global uniform uint ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_UVEC2** = `10`

2-dimensional unsigned integer vector global shader parameter
(`global uniform uvec2 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_UVEC3** = `11`

3-dimensional unsigned integer vector global shader parameter
(`global uniform uvec3 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_UVEC4** = `12`

4-dimensional unsigned integer vector global shader parameter
(`global uniform uvec4 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_FLOAT** = `13`

Single-precision floating-point global shader parameter
(`global uniform float ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_VEC2** = `14`

2-dimensional floating-point vector global shader parameter
(`global uniform vec2 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_VEC3** = `15`

3-dimensional floating-point vector global shader parameter
(`global uniform vec3 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_VEC4** = `16`

4-dimensional floating-point vector global shader parameter
(`global uniform vec4 ...`).

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_COLOR** = `17`

Color global shader parameter (`global uniform vec4 ...`). Equivalent to
`GLOBAL_VAR_TYPE_VEC4<class_RenderingServer_constant_GLOBAL_VAR_TYPE_VEC4>`
in shader code, but exposed as a `Color<class_Color>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_RECT2** = `18`

2-dimensional floating-point rectangle global shader parameter
(`global uniform vec4 ...`). Equivalent to
`GLOBAL_VAR_TYPE_VEC4<class_RenderingServer_constant_GLOBAL_VAR_TYPE_VEC4>`
in shader code, but exposed as a `Rect2<class_Rect2>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_MAT2** = `19`

2×2 matrix global shader parameter (`global uniform mat2 ...`). Exposed
as a `PackedInt32Array<class_PackedInt32Array>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_MAT3** = `20`

3×3 matrix global shader parameter (`global uniform mat3 ...`). Exposed
as a `Basis<class_Basis>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_MAT4** = `21`

4×4 matrix global shader parameter (`global uniform mat4 ...`). Exposed
as a `Projection<class_Projection>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_TRANSFORM\_2D** = `22`

2-dimensional transform global shader parameter
(`global uniform mat2x3 ...`). Exposed as a
`Transform2D<class_Transform2D>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_TRANSFORM** = `23`

3-dimensional transform global shader parameter
(`global uniform mat3x4 ...`). Exposed as a
`Transform3D<class_Transform3D>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_SAMPLER2D** = `24`

2D sampler global shader parameter (`global uniform sampler2D ...`).
Exposed as a `Texture2D<class_Texture2D>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_SAMPLER2DARRAY** = `25`

2D sampler array global shader parameter
(`global uniform sampler2DArray ...`). Exposed as a
`Texture2DArray<class_Texture2DArray>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_SAMPLER3D** = `26`

3D sampler global shader parameter (`global uniform sampler3D ...`).
Exposed as a `Texture3D<class_Texture3D>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_SAMPLERCUBE** = `27`

Cubemap sampler global shader parameter
(`global uniform samplerCube ...`). Exposed as a
`Cubemap<class_Cubemap>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_SAMPLEREXT** = `28`

External sampler global shader parameter
(`global uniform samplerExternalOES ...`). Exposed as a
`ExternalTexture<class_ExternalTexture>` in the editor UI.

classref-enumeration-constant

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**GLOBAL\_VAR\_TYPE\_MAX** = `29`

Represents the size of the
`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **RenderingInfo**: `🔗<enum_RenderingServer_RenderingInfo>`

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_TOTAL\_OBJECTS\_IN\_FRAME** = `0`

Number of objects rendered in the current 3D scene. This varies
depending on camera position and rotation.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_TOTAL\_PRIMITIVES\_IN\_FRAME** = `1`

Number of points, lines, or triangles rendered in the current 3D scene.
This varies depending on camera position and rotation.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_TOTAL\_DRAW\_CALLS\_IN\_FRAME** = `2`

Number of draw calls performed to render in the current 3D scene. This
varies depending on camera position and rotation.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_TEXTURE\_MEM\_USED** = `3`

Texture memory used (in bytes).

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_BUFFER\_MEM\_USED** = `4`

Buffer memory used (in bytes). This includes vertex data, uniform
buffers, and many miscellaneous buffer types used internally.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_VIDEO\_MEM\_USED** = `5`

Video memory used (in bytes). When using the Forward+ or mobile
rendering backends, this is always greater than the sum of
`RENDERING_INFO_TEXTURE_MEM_USED<class_RenderingServer_constant_RENDERING_INFO_TEXTURE_MEM_USED>`
and
`RENDERING_INFO_BUFFER_MEM_USED<class_RenderingServer_constant_RENDERING_INFO_BUFFER_MEM_USED>`,
since there is miscellaneous data not accounted for by those two
metrics. When using the GL Compatibility backend, this is equal to the
sum of
`RENDERING_INFO_TEXTURE_MEM_USED<class_RenderingServer_constant_RENDERING_INFO_TEXTURE_MEM_USED>`
and
`RENDERING_INFO_BUFFER_MEM_USED<class_RenderingServer_constant_RENDERING_INFO_BUFFER_MEM_USED>`.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_PIPELINE\_COMPILATIONS\_CANVAS** = `6`

Number of pipeline compilations that were triggered by the 2D canvas
renderer.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_PIPELINE\_COMPILATIONS\_MESH** = `7`

Number of pipeline compilations that were triggered by loading meshes.
These compilations will show up as longer loading times the first time a
user runs the game and the pipeline is required.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_PIPELINE\_COMPILATIONS\_SURFACE** = `8`

Number of pipeline compilations that were triggered by building the
surface cache before rendering the scene. These compilations will show
up as a stutter when loading an scene the first time a user runs the
game and the pipeline is required.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_PIPELINE\_COMPILATIONS\_DRAW** = `9`

Number of pipeline compilations that were triggered while drawing the
scene. These compilations will show up as stutters during gameplay the
first time a user runs the game and the pipeline is required.

classref-enumeration-constant

`RenderingInfo<enum_RenderingServer_RenderingInfo>`
**RENDERING\_INFO\_PIPELINE\_COMPILATIONS\_SPECIALIZATION** = `10`

Number of pipeline compilations that were triggered to optimize the
current scene. These compilations are done in the background and should
not cause any stutters whatsoever.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PipelineSource**: `🔗<enum_RenderingServer_PipelineSource>`

classref-enumeration-constant

`PipelineSource<enum_RenderingServer_PipelineSource>`
**PIPELINE\_SOURCE\_CANVAS** = `0`

Pipeline compilation that was triggered by the 2D canvas renderer.

classref-enumeration-constant

`PipelineSource<enum_RenderingServer_PipelineSource>`
**PIPELINE\_SOURCE\_MESH** = `1`

Pipeline compilation that was triggered by loading a mesh.

classref-enumeration-constant

`PipelineSource<enum_RenderingServer_PipelineSource>`
**PIPELINE\_SOURCE\_SURFACE** = `2`

Pipeline compilation that was triggered by building the surface cache
before rendering the scene.

classref-enumeration-constant

`PipelineSource<enum_RenderingServer_PipelineSource>`
**PIPELINE\_SOURCE\_DRAW** = `3`

Pipeline compilation that was triggered while drawing the scene.

classref-enumeration-constant

`PipelineSource<enum_RenderingServer_PipelineSource>`
**PIPELINE\_SOURCE\_SPECIALIZATION** = `4`

Pipeline compilation that was triggered to optimize the current scene.

classref-enumeration-constant

`PipelineSource<enum_RenderingServer_PipelineSource>`
**PIPELINE\_SOURCE\_MAX** = `5`

Represents the size of the
`PipelineSource<enum_RenderingServer_PipelineSource>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Features**: `🔗<enum_RenderingServer_Features>`

classref-enumeration-constant

`Features<enum_RenderingServer_Features>` **FEATURE\_SHADERS** = `0`

**Deprecated:** This constant has not been used since Godot 3.0.

classref-enumeration-constant

`Features<enum_RenderingServer_Features>` **FEATURE\_MULTITHREADED** =
`1`

**Deprecated:** This constant has not been used since Godot 3.0.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NO\_INDEX\_ARRAY** = `-1`
`🔗<class_RenderingServer_constant_NO_INDEX_ARRAY>`

Marks an error that shows that the index array is empty.

classref-constant

**ARRAY\_WEIGHTS\_SIZE** = `4`
`🔗<class_RenderingServer_constant_ARRAY_WEIGHTS_SIZE>`

Number of weights/bones per vertex.

classref-constant

**CANVAS\_ITEM\_Z\_MIN** = `-4096`
`🔗<class_RenderingServer_constant_CANVAS_ITEM_Z_MIN>`

The minimum Z-layer for canvas items.

classref-constant

**CANVAS\_ITEM\_Z\_MAX** = `4096`
`🔗<class_RenderingServer_constant_CANVAS_ITEM_Z_MAX>`

The maximum Z-layer for canvas items.

classref-constant

**MAX\_GLOW\_LEVELS** = `7`
`🔗<class_RenderingServer_constant_MAX_GLOW_LEVELS>`

The maximum number of glow levels that can be used with the glow
post-processing effect.

classref-constant

**MAX\_CURSORS** = `8` `🔗<class_RenderingServer_constant_MAX_CURSORS>`

**Deprecated:** This constant is not used by the engine.

classref-constant

**MAX\_2D\_DIRECTIONAL\_LIGHTS** = `8`
`🔗<class_RenderingServer_constant_MAX_2D_DIRECTIONAL_LIGHTS>`

The maximum number of directional lights that can be rendered at a given
time in 2D.

classref-constant

**MAX\_MESH\_SURFACES** = `256`
`🔗<class_RenderingServer_constant_MAX_MESH_SURFACES>`

The maximum number of surfaces a mesh can have.

classref-constant

**MATERIAL\_RENDER\_PRIORITY\_MIN** = `-128`
`🔗<class_RenderingServer_constant_MATERIAL_RENDER_PRIORITY_MIN>`

The minimum renderpriority of all materials.

classref-constant

**MATERIAL\_RENDER\_PRIORITY\_MAX** = `127`
`🔗<class_RenderingServer_constant_MATERIAL_RENDER_PRIORITY_MAX>`

The maximum renderpriority of all materials.

classref-constant

**ARRAY\_CUSTOM\_COUNT** = `4`
`🔗<class_RenderingServer_constant_ARRAY_CUSTOM_COUNT>`

The number of custom data arrays available
(`ARRAY_CUSTOM0<class_RenderingServer_constant_ARRAY_CUSTOM0>`,
`ARRAY_CUSTOM1<class_RenderingServer_constant_ARRAY_CUSTOM1>`,
`ARRAY_CUSTOM2<class_RenderingServer_constant_ARRAY_CUSTOM2>`,
`ARRAY_CUSTOM3<class_RenderingServer_constant_ARRAY_CUSTOM3>`).

classref-constant

**PARTICLES\_EMIT\_FLAG\_POSITION** = `1`
`🔗<class_RenderingServer_constant_PARTICLES_EMIT_FLAG_POSITION>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**PARTICLES\_EMIT\_FLAG\_ROTATION\_SCALE** = `2`
`🔗<class_RenderingServer_constant_PARTICLES_EMIT_FLAG_ROTATION_SCALE>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**PARTICLES\_EMIT\_FLAG\_VELOCITY** = `4`
`🔗<class_RenderingServer_constant_PARTICLES_EMIT_FLAG_VELOCITY>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**PARTICLES\_EMIT\_FLAG\_COLOR** = `8`
`🔗<class_RenderingServer_constant_PARTICLES_EMIT_FLAG_COLOR>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**PARTICLES\_EMIT\_FLAG\_CUSTOM** = `16`
`🔗<class_RenderingServer_constant_PARTICLES_EMIT_FLAG_CUSTOM>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **render\_loop\_enabled**
`🔗<class_RenderingServer_property_render_loop_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_render\_loop\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_render\_loop\_enabled**()

If `false`, disables rendering completely, but the engine logic is still
being processed. You can call
`force_draw<class_RenderingServer_method_force_draw>` to draw a frame
even with rendering disabled.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>`\[`Image<class_Image>`\] **bake\_render\_uv2**(base:
`RID<class_RID>`, material\_overrides:
`Array<class_Array>`\[`RID<class_RID>`\], image\_size:
`Vector2i<class_Vector2i>`)
`🔗<class_RenderingServer_method_bake_render_uv2>`

Bakes the material data of the Mesh passed in the `base` parameter with
optional `material_overrides` to a set of `Image<class_Image>`s of size
`image_size`. Returns an array of `Image<class_Image>`s containing
material properties as specified in
`BakeChannels<enum_RenderingServer_BakeChannels>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **call\_on\_render\_thread**(callable:
`Callable<class_Callable>`)
`🔗<class_RenderingServer_method_call_on_render_thread>`

As the RenderingServer actual logic may run on an separate thread,
accessing its internals from the main (or any other) thread will result
in errors. To make it easier to run code that can safely access the
rendering internals (such as `RenderingDevice<class_RenderingDevice>`
and similar RD classes), push a callable via this function so it will be
executed on the render thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **camera\_attributes\_create**()
`🔗<class_RenderingServer_method_camera_attributes_create>`

Creates a camera attributes object and adds it to the RenderingServer.
It can be accessed with the RID that is returned. This RID will be used
in all `camera_attributes_` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is
`CameraAttributes<class_CameraAttributes>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**camera\_attributes\_set\_auto\_exposure**(camera\_attributes:
`RID<class_RID>`, enable: `bool<class_bool>`, min\_sensitivity:
`float<class_float>`, max\_sensitivity: `float<class_float>`, speed:
`float<class_float>`, scale: `float<class_float>`)
`🔗<class_RenderingServer_method_camera_attributes_set_auto_exposure>`

Sets the parameters to use with the auto-exposure effect. These
parameters take on the same meaning as their counterparts in
`CameraAttributes<class_CameraAttributes>` and
`CameraAttributesPractical<class_CameraAttributesPractical>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**camera\_attributes\_set\_dof\_blur**(camera\_attributes:
`RID<class_RID>`, far\_enable: `bool<class_bool>`, far\_distance:
`float<class_float>`, far\_transition: `float<class_float>`,
near\_enable: `bool<class_bool>`, near\_distance: `float<class_float>`,
near\_transition: `float<class_float>`, amount: `float<class_float>`)
`🔗<class_RenderingServer_method_camera_attributes_set_dof_blur>`

Sets the parameters to use with the DOF blur effect. These parameters
take on the same meaning as their counterparts in
`CameraAttributesPractical<class_CameraAttributesPractical>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**camera\_attributes\_set\_dof\_blur\_bokeh\_shape**(shape:
`DOFBokehShape<enum_RenderingServer_DOFBokehShape>`)
`🔗<class_RenderingServer_method_camera_attributes_set_dof_blur_bokeh_shape>`

Sets the shape of the DOF bokeh pattern. Different shapes may be used to
achieve artistic effect, or to meet performance targets. For more detail
on available options see
`DOFBokehShape<enum_RenderingServer_DOFBokehShape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**camera\_attributes\_set\_dof\_blur\_quality**(quality:
`DOFBlurQuality<enum_RenderingServer_DOFBlurQuality>`, use\_jitter:
`bool<class_bool>`)
`🔗<class_RenderingServer_method_camera_attributes_set_dof_blur_quality>`

Sets the quality level of the DOF blur effect to one of the options in
`DOFBlurQuality<enum_RenderingServer_DOFBlurQuality>`. `use_jitter` can
be used to jitter samples taken during the blur pass to hide artifacts
at the cost of looking more fuzzy.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**camera\_attributes\_set\_exposure**(camera\_attributes:
`RID<class_RID>`, multiplier: `float<class_float>`, normalization:
`float<class_float>`)
`🔗<class_RenderingServer_method_camera_attributes_set_exposure>`

Sets the exposure values that will be used by the renderers. The
normalization amount is used to bake a given Exposure Value (EV) into
rendering calculations to reduce the dynamic range of the scene.

The normalization factor can be calculated from exposure value (EV100)
as follows:

    func get_exposure_normalization(ev100: float):
        return 1.0 / (pow(2.0, ev100) * 1.2)

The exposure value can be calculated from aperture (in f-stops), shutter
speed (in seconds), and sensitivity (in ISO) as follows:

    func get_exposure(aperture: float, shutter_speed: float, sensitivity: float):
        return log((aperture * aperture) / shutter_speed * (100.0 / sensitivity)) / log(2)

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **camera\_create**()
`🔗<class_RenderingServer_method_camera_create>`

Creates a 3D camera and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`camera_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent node is `Camera3D<class_Camera3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_camera\_attributes**(camera:
`RID<class_RID>`, effects: `RID<class_RID>`)
`🔗<class_RenderingServer_method_camera_set_camera_attributes>`

Sets the camera\_attributes created with
`camera_attributes_create<class_RenderingServer_method_camera_attributes_create>`
to the given camera.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_compositor**(camera:
`RID<class_RID>`, compositor: `RID<class_RID>`)
`🔗<class_RenderingServer_method_camera_set_compositor>`

Sets the compositor used by this camera. Equivalent to
`Camera3D.compositor<class_Camera3D_property_compositor>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_cull\_mask**(camera:
`RID<class_RID>`, layers: `int<class_int>`)
`🔗<class_RenderingServer_method_camera_set_cull_mask>`

Sets the cull mask associated with this camera. The cull mask describes
which 3D layers are rendered by this camera. Equivalent to
`Camera3D.cull_mask<class_Camera3D_property_cull_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_environment**(camera:
`RID<class_RID>`, env: `RID<class_RID>`)
`🔗<class_RenderingServer_method_camera_set_environment>`

Sets the environment used by this camera. Equivalent to
`Camera3D.environment<class_Camera3D_property_environment>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_frustum**(camera:
`RID<class_RID>`, size: `float<class_float>`, offset:
`Vector2<class_Vector2>`, z\_near: `float<class_float>`, z\_far:
`float<class_float>`)
`🔗<class_RenderingServer_method_camera_set_frustum>`

Sets camera to use frustum projection. This mode allows adjusting the
`offset` argument to create "tilted frustum" effects.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_orthogonal**(camera:
`RID<class_RID>`, size: `float<class_float>`, z\_near:
`float<class_float>`, z\_far: `float<class_float>`)
`🔗<class_RenderingServer_method_camera_set_orthogonal>`

Sets camera to use orthogonal projection, also known as orthographic
projection. Objects remain the same size on the screen no matter how far
away they are.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_perspective**(camera:
`RID<class_RID>`, fovy\_degrees: `float<class_float>`, z\_near:
`float<class_float>`, z\_far: `float<class_float>`)
`🔗<class_RenderingServer_method_camera_set_perspective>`

Sets camera to use perspective projection. Objects on the screen becomes
smaller when they are far away.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_transform**(camera:
`RID<class_RID>`, transform: `Transform3D<class_Transform3D>`)
`🔗<class_RenderingServer_method_camera_set_transform>`

Sets `Transform3D<class_Transform3D>` of camera.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **camera\_set\_use\_vertical\_aspect**(camera:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_camera_set_use_vertical_aspect>`

If `true`, preserves the horizontal aspect ratio which is equivalent to
`Camera3D.KEEP_WIDTH<class_Camera3D_constant_KEEP_WIDTH>`. If `false`,
preserves the vertical aspect ratio which is equivalent to
`Camera3D.KEEP_HEIGHT<class_Camera3D_constant_KEEP_HEIGHT>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **canvas\_create**()
`🔗<class_RenderingServer_method_canvas_create>`

Creates a canvas and returns the assigned `RID<class_RID>`. It can be
accessed with the RID that is returned. This RID will be used in all
`canvas_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

Canvas has no `Resource<class_Resource>` or `Node<class_Node>`
equivalent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_animation\_slice**(item:
`RID<class_RID>`, animation\_length: `float<class_float>`, slice\_begin:
`float<class_float>`, slice\_end: `float<class_float>`, offset:
`float<class_float>` = 0.0)
`🔗<class_RenderingServer_method_canvas_item_add_animation_slice>`

Subsequent drawing commands will be ignored unless they fall within the
specified animation slice. This is a faster way to implement animations
that loop on background rather than redrawing constantly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_circle**(item:
`RID<class_RID>`, pos: `Vector2<class_Vector2>`, radius:
`float<class_float>`, color: `Color<class_Color>`, antialiased:
`bool<class_bool>` = false)
`🔗<class_RenderingServer_method_canvas_item_add_circle>`

Draws a circle on the `CanvasItem<class_CanvasItem>` pointed to by the
`item` `RID<class_RID>`. See also
`CanvasItem.draw_circle<class_CanvasItem_method_draw_circle>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_clip\_ignore**(item:
`RID<class_RID>`, ignore: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_add_clip_ignore>`

If `ignore` is `true`, ignore clipping on items drawn with this canvas
item until this is called again with `ignore` set to false.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_add\_lcd\_texture\_rect\_region**(item:
`RID<class_RID>`, rect: `Rect2<class_Rect2>`, texture: `RID<class_RID>`,
src\_rect: `Rect2<class_Rect2>`, modulate: `Color<class_Color>`)
`🔗<class_RenderingServer_method_canvas_item_add_lcd_texture_rect_region>`

See also
`CanvasItem.draw_lcd_texture_rect_region<class_CanvasItem_method_draw_lcd_texture_rect_region>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_line**(item:
`RID<class_RID>`, from: `Vector2<class_Vector2>`, to:
`Vector2<class_Vector2>`, color: `Color<class_Color>`, width:
`float<class_float>` = -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_RenderingServer_method_canvas_item_add_line>`

Draws a line on the `CanvasItem<class_CanvasItem>` pointed to by the
`item` `RID<class_RID>`. See also
`CanvasItem.draw_line<class_CanvasItem_method_draw_line>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_mesh**(item:
`RID<class_RID>`, mesh: `RID<class_RID>`, transform:
`Transform2D<class_Transform2D>` = Transform2D(1, 0, 0, 1, 0, 0),
modulate: `Color<class_Color>` = Color(1, 1, 1, 1), texture:
`RID<class_RID>` = RID())
`🔗<class_RenderingServer_method_canvas_item_add_mesh>`

Draws a mesh created with
`mesh_create<class_RenderingServer_method_mesh_create>` with given
`transform`, `modulate` color, and `texture`. This is used internally by
`MeshInstance2D<class_MeshInstance2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_add\_msdf\_texture\_rect\_region**(item:
`RID<class_RID>`, rect: `Rect2<class_Rect2>`, texture: `RID<class_RID>`,
src\_rect: `Rect2<class_Rect2>`, modulate: `Color<class_Color>` =
Color(1, 1, 1, 1), outline\_size: `int<class_int>` = 0, px\_range:
`float<class_float>` = 1.0, scale: `float<class_float>` = 1.0)
`🔗<class_RenderingServer_method_canvas_item_add_msdf_texture_rect_region>`

See also
`CanvasItem.draw_msdf_texture_rect_region<class_CanvasItem_method_draw_msdf_texture_rect_region>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_multiline**(item:
`RID<class_RID>`, points:
`PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, width: `float<class_float>`
= -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_RenderingServer_method_canvas_item_add_multiline>`

Draws a 2D multiline on the `CanvasItem<class_CanvasItem>` pointed to by
the `item` `RID<class_RID>`. See also
`CanvasItem.draw_multiline<class_CanvasItem_method_draw_multiline>` and
`CanvasItem.draw_multiline_colors<class_CanvasItem_method_draw_multiline_colors>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_multimesh**(item:
`RID<class_RID>`, mesh: `RID<class_RID>`, texture: `RID<class_RID>` =
RID()) `🔗<class_RenderingServer_method_canvas_item_add_multimesh>`

Draws a 2D `MultiMesh<class_MultiMesh>` on the
`CanvasItem<class_CanvasItem>` pointed to by the `item`
`RID<class_RID>`. See also
`CanvasItem.draw_multimesh<class_CanvasItem_method_draw_multimesh>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_nine\_patch**(item:
`RID<class_RID>`, rect: `Rect2<class_Rect2>`, source:
`Rect2<class_Rect2>`, texture: `RID<class_RID>`, topleft:
`Vector2<class_Vector2>`, bottomright: `Vector2<class_Vector2>`,
x\_axis\_mode:
`NinePatchAxisMode<enum_RenderingServer_NinePatchAxisMode>` = 0,
y\_axis\_mode:
`NinePatchAxisMode<enum_RenderingServer_NinePatchAxisMode>` = 0,
draw\_center: `bool<class_bool>` = true, modulate: `Color<class_Color>`
= Color(1, 1, 1, 1))
`🔗<class_RenderingServer_method_canvas_item_add_nine_patch>`

Draws a nine-patch rectangle on the `CanvasItem<class_CanvasItem>`
pointed to by the `item` `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_particles**(item:
`RID<class_RID>`, particles: `RID<class_RID>`, texture:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_item_add_particles>`

Draws particles on the `CanvasItem<class_CanvasItem>` pointed to by the
`item` `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_polygon**(item:
`RID<class_RID>`, points:
`PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, uvs:
`PackedVector2Array<class_PackedVector2Array>` = PackedVector2Array(),
texture: `RID<class_RID>` = RID())
`🔗<class_RenderingServer_method_canvas_item_add_polygon>`

Draws a 2D polygon on the `CanvasItem<class_CanvasItem>` pointed to by
the `item` `RID<class_RID>`. If you need more flexibility (such as being
able to use bones), use
`canvas_item_add_triangle_array<class_RenderingServer_method_canvas_item_add_triangle_array>`
instead. See also
`CanvasItem.draw_polygon<class_CanvasItem_method_draw_polygon>`.

\*\*Note:\*\* If you frequently redraw the same polygon with a large
number of vertices, consider pre-calculating the triangulation with
`Geometry2D.triangulate_polygon<class_Geometry2D_method_triangulate_polygon>`
and using `CanvasItem.draw_mesh<class_CanvasItem_method_draw_mesh>`,
`CanvasItem.draw_multimesh<class_CanvasItem_method_draw_multimesh>`, or
`canvas_item_add_triangle_array<class_RenderingServer_method_canvas_item_add_triangle_array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_polyline**(item:
`RID<class_RID>`, points:
`PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, width: `float<class_float>`
= -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_RenderingServer_method_canvas_item_add_polyline>`

Draws a 2D polyline on the `CanvasItem<class_CanvasItem>` pointed to by
the `item` `RID<class_RID>`. See also
`CanvasItem.draw_polyline<class_CanvasItem_method_draw_polyline>` and
`CanvasItem.draw_polyline_colors<class_CanvasItem_method_draw_polyline_colors>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_primitive**(item:
`RID<class_RID>`, points:
`PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, uvs:
`PackedVector2Array<class_PackedVector2Array>`, texture:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_item_add_primitive>`

Draws a 2D primitive on the `CanvasItem<class_CanvasItem>` pointed to by
the `item` `RID<class_RID>`. See also
`CanvasItem.draw_primitive<class_CanvasItem_method_draw_primitive>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_rect**(item:
`RID<class_RID>`, rect: `Rect2<class_Rect2>`, color:
`Color<class_Color>`, antialiased: `bool<class_bool>` = false)
`🔗<class_RenderingServer_method_canvas_item_add_rect>`

Draws a rectangle on the `CanvasItem<class_CanvasItem>` pointed to by
the `item` `RID<class_RID>`. See also
`CanvasItem.draw_rect<class_CanvasItem_method_draw_rect>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_set\_transform**(item:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_canvas_item_add_set_transform>`

Sets a `Transform2D<class_Transform2D>` that will be used to transform
subsequent canvas item commands.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_texture\_rect**(item:
`RID<class_RID>`, rect: `Rect2<class_Rect2>`, texture: `RID<class_RID>`,
tile: `bool<class_bool>` = false, modulate: `Color<class_Color>` =
Color(1, 1, 1, 1), transpose: `bool<class_bool>` = false)
`🔗<class_RenderingServer_method_canvas_item_add_texture_rect>`

Draws a 2D textured rectangle on the `CanvasItem<class_CanvasItem>`
pointed to by the `item` `RID<class_RID>`. See also
`CanvasItem.draw_texture_rect<class_CanvasItem_method_draw_texture_rect>`
and `Texture2D.draw_rect<class_Texture2D_method_draw_rect>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_add\_texture\_rect\_region**(item: `RID<class_RID>`,
rect: `Rect2<class_Rect2>`, texture: `RID<class_RID>`, src\_rect:
`Rect2<class_Rect2>`, modulate: `Color<class_Color>` = Color(1, 1, 1,
1), transpose: `bool<class_bool>` = false, clip\_uv: `bool<class_bool>`
= true)
`🔗<class_RenderingServer_method_canvas_item_add_texture_rect_region>`

Draws the specified region of a 2D textured rectangle on the
`CanvasItem<class_CanvasItem>` pointed to by the `item`
`RID<class_RID>`. See also
`CanvasItem.draw_texture_rect_region<class_CanvasItem_method_draw_texture_rect_region>`
and
`Texture2D.draw_rect_region<class_Texture2D_method_draw_rect_region>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_add\_triangle\_array**(item:
`RID<class_RID>`, indices: `PackedInt32Array<class_PackedInt32Array>`,
points: `PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, uvs:
`PackedVector2Array<class_PackedVector2Array>` = PackedVector2Array(),
bones: `PackedInt32Array<class_PackedInt32Array>` = PackedInt32Array(),
weights: `PackedFloat32Array<class_PackedFloat32Array>` =
PackedFloat32Array(), texture: `RID<class_RID>` = RID(), count:
`int<class_int>` = -1)
`🔗<class_RenderingServer_method_canvas_item_add_triangle_array>`

Draws a triangle array on the `CanvasItem<class_CanvasItem>` pointed to
by the `item` `RID<class_RID>`. This is internally used by
`Line2D<class_Line2D>` and `StyleBoxFlat<class_StyleBoxFlat>` for
rendering.
`canvas_item_add_triangle_array<class_RenderingServer_method_canvas_item_add_triangle_array>`
is highly flexible, but more complex to use than
`canvas_item_add_polygon<class_RenderingServer_method_canvas_item_add_polygon>`.

\*\*Note:\*\* `count` is unused and can be left unspecified.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_attach\_skeleton**(item:
`RID<class_RID>`, skeleton: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_item_attach_skeleton>`

Attaches a skeleton to the `CanvasItem<class_CanvasItem>`. Removes the
previous skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_clear**(item:
`RID<class_RID>`) `🔗<class_RenderingServer_method_canvas_item_clear>`

Clears the `CanvasItem<class_CanvasItem>` and removes all commands in
it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **canvas\_item\_create**()
`🔗<class_RenderingServer_method_canvas_item_create>`

Creates a new CanvasItem instance and returns its `RID<class_RID>`. It
can be accessed with the RID that is returned. This RID will be used in
all `canvas_item_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent node is `CanvasItem<class_CanvasItem>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_reset\_physics\_interpolation**(item: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_item_reset_physics_interpolation>`

Prevents physics interpolation for the current physics tick.

This is useful when moving a canvas item to a new location, to give an
instantaneous change rather than interpolation from the previous
location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_canvas\_group\_mode**(item: `RID<class_RID>`, mode:
`CanvasGroupMode<enum_RenderingServer_CanvasGroupMode>`, clear\_margin:
`float<class_float>` = 5.0, fit\_empty: `bool<class_bool>` = false,
fit\_margin: `float<class_float>` = 0.0, blur\_mipmaps:
`bool<class_bool>` = false)
`🔗<class_RenderingServer_method_canvas_item_set_canvas_group_mode>`

Sets the canvas group mode used during 2D rendering for the canvas item
specified by the `item` RID. For faster but more limited clipping, use
`canvas_item_set_clip<class_RenderingServer_method_canvas_item_set_clip>`
instead.

\*\*Note:\*\* The equivalent node functionality is found in
`CanvasGroup<class_CanvasGroup>` and
`CanvasItem.clip_children<class_CanvasItem_property_clip_children>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_clip**(item:
`RID<class_RID>`, clip: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_set_clip>`

If `clip` is `true`, makes the canvas item specified by the `item` RID
not draw anything outside of its rect's coordinates. This clipping is
fast, but works only with axis-aligned rectangles. This means that
rotation is ignored by the clipping rectangle. For more advanced
clipping shapes, use
`canvas_item_set_canvas_group_mode<class_RenderingServer_method_canvas_item_set_canvas_group_mode>`
instead.

\*\*Note:\*\* The equivalent node functionality is found in
`Label.clip_text<class_Label_property_clip_text>`,
`RichTextLabel<class_RichTextLabel>` (always enabled) and more.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_copy\_to\_backbuffer**(item: `RID<class_RID>`,
enabled: `bool<class_bool>`, rect: `Rect2<class_Rect2>`)
`🔗<class_RenderingServer_method_canvas_item_set_copy_to_backbuffer>`

Sets the `CanvasItem<class_CanvasItem>` to copy a rect to the
backbuffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_custom\_rect**(item:
`RID<class_RID>`, use\_custom\_rect: `bool<class_bool>`, rect:
`Rect2<class_Rect2>` = Rect2(0, 0, 0, 0))
`🔗<class_RenderingServer_method_canvas_item_set_custom_rect>`

If `use_custom_rect` is `true`, sets the custom visibility rectangle
(used for culling) to `rect` for the canvas item specified by `item`.
Setting a custom visibility rect can reduce CPU load when drawing lots
of 2D instances. If `use_custom_rect` is `false`, automatically computes
a visibility rectangle based on the canvas item's draw commands.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_default\_texture\_filter**(item: `RID<class_RID>`,
filter:
`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`)
`🔗<class_RenderingServer_method_canvas_item_set_default_texture_filter>`

Sets the default texture filter mode for the canvas item specified by
the `item` RID. Equivalent to
`CanvasItem.texture_filter<class_CanvasItem_property_texture_filter>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_default\_texture\_repeat**(item: `RID<class_RID>`,
repeat:
`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`)
`🔗<class_RenderingServer_method_canvas_item_set_default_texture_repeat>`

Sets the default texture repeat mode for the canvas item specified by
the `item` RID. Equivalent to
`CanvasItem.texture_repeat<class_CanvasItem_property_texture_repeat>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_distance\_field\_mode**(item: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_set_distance_field_mode>`

If `enabled` is `true`, enables multichannel signed distance field
rendering mode for the canvas item specified by the `item` RID. This is
meant to be used for font rendering, or with specially generated images
using [msdfgen](https://github.com/Chlumsky/msdfgen).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_draw\_behind\_parent**(item: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_set_draw_behind_parent>`

If `enabled` is `true`, draws the canvas item specified by the `item`
RID behind its parent. Equivalent to
`CanvasItem.show_behind_parent<class_CanvasItem_property_show_behind_parent>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_draw\_index**(item:
`RID<class_RID>`, index: `int<class_int>`)
`🔗<class_RenderingServer_method_canvas_item_set_draw_index>`

Sets the index for the `CanvasItem<class_CanvasItem>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_interpolated**(item:
`RID<class_RID>`, interpolated: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_set_interpolated>`

If `interpolated` is `true`, turns on physics interpolation for the
canvas item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_light\_mask**(item:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_RenderingServer_method_canvas_item_set_light_mask>`

Sets the light `mask` for the canvas item specified by the `item` RID.
Equivalent to
`CanvasItem.light_mask<class_CanvasItem_property_light_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_material**(item:
`RID<class_RID>`, material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_item_set_material>`

Sets a new `material` to the canvas item specified by the `item` RID.
Equivalent to `CanvasItem.material<class_CanvasItem_property_material>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_modulate**(item:
`RID<class_RID>`, color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_canvas_item_set_modulate>`

Multiplies the color of the canvas item specified by the `item` RID,
while affecting its children. See also
`canvas_item_set_self_modulate<class_RenderingServer_method_canvas_item_set_self_modulate>`.
Equivalent to `CanvasItem.modulate<class_CanvasItem_property_modulate>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_parent**(item:
`RID<class_RID>`, parent: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_item_set_parent>`

Sets a parent `CanvasItem<class_CanvasItem>` to the
`CanvasItem<class_CanvasItem>`. The item will inherit transform,
modulation and visibility from its parent, like
`CanvasItem<class_CanvasItem>` nodes in the scene tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_self\_modulate**(item:
`RID<class_RID>`, color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_canvas_item_set_self_modulate>`

Multiplies the color of the canvas item specified by the `item` RID,
without affecting its children. See also
`canvas_item_set_modulate<class_RenderingServer_method_canvas_item_set_modulate>`.
Equivalent to
`CanvasItem.self_modulate<class_CanvasItem_property_self_modulate>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_sort\_children\_by\_y**(item: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_set_sort_children_by_y>`

If `enabled` is `true`, child nodes with the lowest Y position are drawn
before those with a higher Y position. Y-sorting only affects children
that inherit from the canvas item specified by the `item` RID, not the
canvas item itself. Equivalent to
`CanvasItem.y_sort_enabled<class_CanvasItem_property_y_sort_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_transform**(item:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_canvas_item_set_transform>`

Sets the `transform` of the canvas item specified by the `item` RID.
This affects where and how the item will be drawn. Child canvas items'
transforms are multiplied by their parent's transform. Equivalent to
`Node2D.transform<class_Node2D_property_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_use\_parent\_material**(item: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_set_use_parent_material>`

Sets if the `CanvasItem<class_CanvasItem>` uses its parent's material.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_visibility\_layer**(item:
`RID<class_RID>`, visibility\_layer: `int<class_int>`)
`🔗<class_RenderingServer_method_canvas_item_set_visibility_layer>`

Sets the rendering visibility layer associated with this
`CanvasItem<class_CanvasItem>`. Only `Viewport<class_Viewport>` nodes
with a matching rendering mask will render this
`CanvasItem<class_CanvasItem>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_visibility\_notifier**(item: `RID<class_RID>`,
enable: `bool<class_bool>`, area: `Rect2<class_Rect2>`, enter\_callable:
`Callable<class_Callable>`, exit\_callable: `Callable<class_Callable>`)
`🔗<class_RenderingServer_method_canvas_item_set_visibility_notifier>`

Sets the given `CanvasItem<class_CanvasItem>` as visibility notifier.
`area` defines the area of detecting visibility. `enter_callable` is
called when the `CanvasItem<class_CanvasItem>` enters the screen,
`exit_callable` is called when the `CanvasItem<class_CanvasItem>` exits
the screen. If `enable` is `false`, the item will no longer function as
notifier.

This method can be used to manually mimic
`VisibleOnScreenNotifier2D<class_VisibleOnScreenNotifier2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_visible**(item:
`RID<class_RID>`, visible: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_set_visible>`

Sets the visibility of the `CanvasItem<class_CanvasItem>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_set\_z\_as\_relative\_to\_parent**(item:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_item_set_z_as_relative_to_parent>`

If this is enabled, the Z index of the parent will be added to the
children's Z index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_item\_set\_z\_index**(item:
`RID<class_RID>`, z\_index: `int<class_int>`)
`🔗<class_RenderingServer_method_canvas_item_set_z_index>`

Sets the `CanvasItem<class_CanvasItem>`'s Z index, i.e. its draw order
(lower indexes are drawn first).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_item\_transform\_physics\_interpolation**(item:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_canvas_item_transform_physics_interpolation>`

Transforms both the current and previous stored transform for a canvas
item.

This allows transforming a canvas item without creating a "glitch" in
the interpolation, which is particularly useful for large worlds
utilizing a shifting origin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_attach\_to\_canvas**(light:
`RID<class_RID>`, canvas: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_light_attach_to_canvas>`

Attaches the canvas light to the canvas. Removes it from its previous
canvas.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **canvas\_light\_create**()
`🔗<class_RenderingServer_method_canvas_light_create>`

Creates a canvas light and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`canvas_light_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent node is `Light2D<class_Light2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_attach\_to\_canvas**(occluder:
`RID<class_RID>`, canvas: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_attach_to_canvas>`

Attaches a light occluder to the canvas. Removes it from its previous
canvas.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **canvas\_light\_occluder\_create**()
`🔗<class_RenderingServer_method_canvas_light_occluder_create>`

Creates a light occluder and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`canvas_light_occluder_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent node is
`LightOccluder2D<class_LightOccluder2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_reset\_physics\_interpolation**(occluder:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_reset_physics_interpolation>`

Prevents physics interpolation for the current physics tick.

This is useful when moving an occluder to a new location, to give an
instantaneous change rather than interpolation from the previous
location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_set\_as\_sdf\_collision**(occluder:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_set_as_sdf_collision>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_set\_enabled**(occluder: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_set_enabled>`

Enables or disables light occluder.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_set\_interpolated**(occluder:
`RID<class_RID>`, interpolated: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_set_interpolated>`

If `interpolated` is `true`, turns on physics interpolation for the
light occluder.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_set\_light\_mask**(occluder:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_set_light_mask>`

The light mask. See `LightOccluder2D<class_LightOccluder2D>` for more
information on light masks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_set\_polygon**(occluder: `RID<class_RID>`,
polygon: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_set_polygon>`

Sets a light occluder's polygon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_set\_transform**(occluder: `RID<class_RID>`,
transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_set_transform>`

Sets a light occluder's `Transform2D<class_Transform2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_occluder\_transform\_physics\_interpolation**(occluder:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_canvas_light_occluder_transform_physics_interpolation>`

Transforms both the current and previous stored transform for a light
occluder.

This allows transforming an occluder without creating a "glitch" in the
interpolation, which is particularly useful for large worlds utilizing a
shifting origin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_reset\_physics\_interpolation**(light:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_light_reset_physics_interpolation>`

Prevents physics interpolation for the current physics tick.

This is useful when moving a canvas item to a new location, to give an
instantaneous change rather than interpolation from the previous
location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_blend\_mode**(light:
`RID<class_RID>`, mode:
`CanvasLightBlendMode<enum_RenderingServer_CanvasLightBlendMode>`)
`🔗<class_RenderingServer_method_canvas_light_set_blend_mode>`

Sets the blend mode for the given canvas light. See
`CanvasLightBlendMode<enum_RenderingServer_CanvasLightBlendMode>` for
options. Equivalent to
`Light2D.blend_mode<class_Light2D_property_blend_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_color**(light:
`RID<class_RID>`, color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_canvas_light_set_color>`

Sets the color for a light.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_enabled**(light:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_light_set_enabled>`

Enables or disables a canvas light.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_energy**(light:
`RID<class_RID>`, energy: `float<class_float>`)
`🔗<class_RenderingServer_method_canvas_light_set_energy>`

Sets a canvas light's energy.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_height**(light:
`RID<class_RID>`, height: `float<class_float>`)
`🔗<class_RenderingServer_method_canvas_light_set_height>`

Sets a canvas light's height.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_interpolated**(light:
`RID<class_RID>`, interpolated: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_light_set_interpolated>`

If `interpolated` is `true`, turns on physics interpolation for the
canvas light.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_set\_item\_cull\_mask**(light: `RID<class_RID>`, mask:
`int<class_int>`)
`🔗<class_RenderingServer_method_canvas_light_set_item_cull_mask>`

The light mask. See `LightOccluder2D<class_LightOccluder2D>` for more
information on light masks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_set\_item\_shadow\_cull\_mask**(light:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_RenderingServer_method_canvas_light_set_item_shadow_cull_mask>`

The binary mask used to determine which layers this canvas light's
shadows affects. See `LightOccluder2D<class_LightOccluder2D>` for more
information on light masks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_layer\_range**(light:
`RID<class_RID>`, min\_layer: `int<class_int>`, max\_layer:
`int<class_int>`)
`🔗<class_RenderingServer_method_canvas_light_set_layer_range>`

The layer range that gets rendered with this light.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_mode**(light:
`RID<class_RID>`, mode:
`CanvasLightMode<enum_RenderingServer_CanvasLightMode>`)
`🔗<class_RenderingServer_method_canvas_light_set_mode>`

The mode of the light, see
`CanvasLightMode<enum_RenderingServer_CanvasLightMode>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_shadow\_color**(light:
`RID<class_RID>`, color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_canvas_light_set_shadow_color>`

Sets the color of the canvas light's shadow.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_shadow\_enabled**(light:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_light_set_shadow_enabled>`

Enables or disables the canvas light's shadow.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_shadow\_filter**(light:
`RID<class_RID>`, filter:
`CanvasLightShadowFilter<enum_RenderingServer_CanvasLightShadowFilter>`)
`🔗<class_RenderingServer_method_canvas_light_set_shadow_filter>`

Sets the canvas light's shadow's filter, see
`CanvasLightShadowFilter<enum_RenderingServer_CanvasLightShadowFilter>`
constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_shadow\_smooth**(light:
`RID<class_RID>`, smooth: `float<class_float>`)
`🔗<class_RenderingServer_method_canvas_light_set_shadow_smooth>`

Smoothens the shadow. The lower, the smoother.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_texture**(light:
`RID<class_RID>`, texture: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_light_set_texture>`

Sets the texture to be used by a `PointLight2D<class_PointLight2D>`.
Equivalent to
`PointLight2D.texture<class_PointLight2D_property_texture>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_texture\_offset**(light:
`RID<class_RID>`, offset: `Vector2<class_Vector2>`)
`🔗<class_RenderingServer_method_canvas_light_set_texture_offset>`

Sets the offset of a `PointLight2D<class_PointLight2D>`'s texture.
Equivalent to `PointLight2D.offset<class_PointLight2D_property_offset>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_texture\_scale**(light:
`RID<class_RID>`, scale: `float<class_float>`)
`🔗<class_RenderingServer_method_canvas_light_set_texture_scale>`

Sets the scale factor of a `PointLight2D<class_PointLight2D>`'s texture.
Equivalent to
`PointLight2D.texture_scale<class_PointLight2D_property_texture_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_transform**(light:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_canvas_light_set_transform>`

Sets the canvas light's `Transform2D<class_Transform2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_light\_set\_z\_range**(light:
`RID<class_RID>`, min\_z: `int<class_int>`, max\_z: `int<class_int>`)
`🔗<class_RenderingServer_method_canvas_light_set_z_range>`

Sets the Z range of objects that will be affected by this light.
Equivalent to `Light2D.range_z_min<class_Light2D_property_range_z_min>`
and `Light2D.range_z_max<class_Light2D_property_range_z_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_light\_transform\_physics\_interpolation**(light:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_canvas_light_transform_physics_interpolation>`

Transforms both the current and previous stored transform for a canvas
light.

This allows transforming a light without creating a "glitch" in the
interpolation, which is particularly useful for large worlds utilizing a
shifting origin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **canvas\_occluder\_polygon\_create**()
`🔗<class_RenderingServer_method_canvas_occluder_polygon_create>`

Creates a new light occluder polygon and adds it to the RenderingServer.
It can be accessed with the RID that is returned. This RID will be used
in all `canvas_occluder_polygon_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is
`OccluderPolygon2D<class_OccluderPolygon2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_occluder\_polygon\_set\_cull\_mode**(occluder\_polygon:
`RID<class_RID>`, mode:
`CanvasOccluderPolygonCullMode<enum_RenderingServer_CanvasOccluderPolygonCullMode>`)
`🔗<class_RenderingServer_method_canvas_occluder_polygon_set_cull_mode>`

Sets an occluder polygons cull mode. See
`CanvasOccluderPolygonCullMode<enum_RenderingServer_CanvasOccluderPolygonCullMode>`
constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_occluder\_polygon\_set\_shape**(occluder\_polygon:
`RID<class_RID>`, shape: `PackedVector2Array<class_PackedVector2Array>`,
closed: `bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_occluder_polygon_set_shape>`

Sets the shape of the occluder polygon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_set\_disable\_scale**(disable:
`bool<class_bool>`)
`🔗<class_RenderingServer_method_canvas_set_disable_scale>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_set\_item\_mirroring**(canvas:
`RID<class_RID>`, item: `RID<class_RID>`, mirroring:
`Vector2<class_Vector2>`)
`🔗<class_RenderingServer_method_canvas_set_item_mirroring>`

A copy of the canvas item will be drawn with a local offset of the
`mirroring`.

\*\*Note:\*\* This is equivalent to calling
`canvas_set_item_repeat<class_RenderingServer_method_canvas_set_item_repeat>`
like `canvas_set_item_repeat(item, mirroring, 1)`, with an additional
check ensuring `canvas` is a parent of `item`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_set\_item\_repeat**(item:
`RID<class_RID>`, repeat\_size: `Vector2<class_Vector2>`, repeat\_times:
`int<class_int>`)
`🔗<class_RenderingServer_method_canvas_set_item_repeat>`

A copy of the canvas item will be drawn with a local offset of the
`repeat_size` by the number of times of the `repeat_times`. As the
`repeat_times` increases, the copies will spread away from the origin
texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_set\_modulate**(canvas:
`RID<class_RID>`, color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_canvas_set_modulate>`

Modulates all colors in the given canvas.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **canvas\_set\_shadow\_texture\_size**(size:
`int<class_int>`)
`🔗<class_RenderingServer_method_canvas_set_shadow_texture_size>`

Sets the
`ProjectSettings.rendering/2d/shadow_atlas/size<class_ProjectSettings_property_rendering/2d/shadow_atlas/size>`
to use for `Light2D<class_Light2D>` shadow rendering (in pixels). The
value is rounded up to the nearest power of 2.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **canvas\_texture\_create**()
`🔗<class_RenderingServer_method_canvas_texture_create>`

Creates a canvas texture and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`canvas_texture_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method. See also
`texture_2d_create<class_RenderingServer_method_texture_2d_create>`.

\*\*Note:\*\* The equivalent resource is
`CanvasTexture<class_CanvasTexture>` and is only meant to be used in 2D
rendering, not 3D.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_texture\_set\_channel**(canvas\_texture: `RID<class_RID>`,
channel:
`CanvasTextureChannel<enum_RenderingServer_CanvasTextureChannel>`,
texture: `RID<class_RID>`)
`🔗<class_RenderingServer_method_canvas_texture_set_channel>`

Sets the `channel`'s `texture` for the canvas texture specified by the
`canvas_texture` RID. Equivalent to
`CanvasTexture.diffuse_texture<class_CanvasTexture_property_diffuse_texture>`,
`CanvasTexture.normal_texture<class_CanvasTexture_property_normal_texture>`
and
`CanvasTexture.specular_texture<class_CanvasTexture_property_specular_texture>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_texture\_set\_shading\_parameters**(canvas\_texture:
`RID<class_RID>`, base\_color: `Color<class_Color>`, shininess:
`float<class_float>`)
`🔗<class_RenderingServer_method_canvas_texture_set_shading_parameters>`

Sets the `base_color` and `shininess` to use for the canvas texture
specified by the `canvas_texture` RID. Equivalent to
`CanvasTexture.specular_color<class_CanvasTexture_property_specular_color>`
and
`CanvasTexture.specular_shininess<class_CanvasTexture_property_specular_shininess>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_texture\_set\_texture\_filter**(canvas\_texture:
`RID<class_RID>`, filter:
`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`)
`🔗<class_RenderingServer_method_canvas_texture_set_texture_filter>`

Sets the texture `filter` mode to use for the canvas texture specified
by the `canvas_texture` RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**canvas\_texture\_set\_texture\_repeat**(canvas\_texture:
`RID<class_RID>`, repeat:
`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`)
`🔗<class_RenderingServer_method_canvas_texture_set_texture_repeat>`

Sets the texture `repeat` mode to use for the canvas texture specified
by the `canvas_texture` RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **compositor\_create**()
`🔗<class_RenderingServer_method_compositor_create>`

Creates a new compositor and adds it to the RenderingServer. It can be
accessed with the RID that is returned.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **compositor\_effect\_create**()
`🔗<class_RenderingServer_method_compositor_effect_create>`

Creates a new rendering effect and adds it to the RenderingServer. It
can be accessed with the RID that is returned.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **compositor\_effect\_set\_callback**(effect:
`RID<class_RID>`, callback\_type:
`CompositorEffectCallbackType<enum_RenderingServer_CompositorEffectCallbackType>`,
callback: `Callable<class_Callable>`)
`🔗<class_RenderingServer_method_compositor_effect_set_callback>`

Sets the callback type (`callback_type`) and callback method(`callback`)
for this rendering effect.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **compositor\_effect\_set\_enabled**(effect:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_compositor_effect_set_enabled>`

Enables/disables this rendering effect.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **compositor\_effect\_set\_flag**(effect:
`RID<class_RID>`, flag:
`CompositorEffectFlags<enum_RenderingServer_CompositorEffectFlags>`,
set: `bool<class_bool>`)
`🔗<class_RenderingServer_method_compositor_effect_set_flag>`

Sets the flag (`flag`) for this rendering effect to `true` or `false`
(`set`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**compositor\_set\_compositor\_effects**(compositor: `RID<class_RID>`,
effects: `Array<class_Array>`\[`RID<class_RID>`\])
`🔗<class_RenderingServer_method_compositor_set_compositor_effects>`

Sets the compositor effects for the specified compositor RID. `effects`
should be an array containing RIDs created with
`compositor_effect_create<class_RenderingServer_method_compositor_effect_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RenderingDevice<class_RenderingDevice>`
**create\_local\_rendering\_device**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_create_local_rendering_device>`

Creates a RenderingDevice that can be used to do draw and compute
operations on a separate thread. Cannot draw to the screen nor share
data with the global RenderingDevice.

\*\*Note:\*\* When using the OpenGL backend or when running in headless
mode, this function always returns `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **debug\_canvas\_item\_get\_rect**(item:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_debug_canvas_item_get_rect>`

Returns the bounding rectangle for a canvas item in local space, as
calculated by the renderer. This bound is used internally for culling.

\*\*Warning:\*\* This function is intended for debugging in the editor,
and will pass through and return a zero `Rect2<class_Rect2>` in exported
projects.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **decal\_create**()
`🔗<class_RenderingServer_method_decal_create>`

Creates a decal and adds it to the RenderingServer. It can be accessed
with the RID that is returned. This RID will be used in all `decal_*`
RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach this decal to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

\*\*Note:\*\* The equivalent node is `Decal<class_Decal>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_albedo\_mix**(decal:
`RID<class_RID>`, albedo\_mix: `float<class_float>`)
`🔗<class_RenderingServer_method_decal_set_albedo_mix>`

Sets the `albedo_mix` in the decal specified by the `decal` RID.
Equivalent to `Decal.albedo_mix<class_Decal_property_albedo_mix>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_cull\_mask**(decal:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_RenderingServer_method_decal_set_cull_mask>`

Sets the cull `mask` in the decal specified by the `decal` RID.
Equivalent to `Decal.cull_mask<class_Decal_property_cull_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_distance\_fade**(decal:
`RID<class_RID>`, enabled: `bool<class_bool>`, begin:
`float<class_float>`, length: `float<class_float>`)
`🔗<class_RenderingServer_method_decal_set_distance_fade>`

Sets the distance fade parameters in the decal specified by the `decal`
RID. Equivalent to
`Decal.distance_fade_enabled<class_Decal_property_distance_fade_enabled>`,
`Decal.distance_fade_begin<class_Decal_property_distance_fade_begin>`
and
`Decal.distance_fade_length<class_Decal_property_distance_fade_length>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_emission\_energy**(decal:
`RID<class_RID>`, energy: `float<class_float>`)
`🔗<class_RenderingServer_method_decal_set_emission_energy>`

Sets the emission `energy` in the decal specified by the `decal` RID.
Equivalent to
`Decal.emission_energy<class_Decal_property_emission_energy>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_fade**(decal: `RID<class_RID>`,
above: `float<class_float>`, below: `float<class_float>`)
`🔗<class_RenderingServer_method_decal_set_fade>`

Sets the upper fade (`above`) and lower fade (`below`) in the decal
specified by the `decal` RID. Equivalent to
`Decal.upper_fade<class_Decal_property_upper_fade>` and
`Decal.lower_fade<class_Decal_property_lower_fade>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_modulate**(decal:
`RID<class_RID>`, color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_decal_set_modulate>`

Sets the color multiplier in the decal specified by the `decal` RID to
`color`. Equivalent to `Decal.modulate<class_Decal_property_modulate>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_normal\_fade**(decal:
`RID<class_RID>`, fade: `float<class_float>`)
`🔗<class_RenderingServer_method_decal_set_normal_fade>`

Sets the normal `fade` in the decal specified by the `decal` RID.
Equivalent to `Decal.normal_fade<class_Decal_property_normal_fade>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_size**(decal: `RID<class_RID>`,
size: `Vector3<class_Vector3>`)
`🔗<class_RenderingServer_method_decal_set_size>`

Sets the `size` of the decal specified by the `decal` RID. Equivalent to
`Decal.size<class_Decal_property_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decal\_set\_texture**(decal:
`RID<class_RID>`, type:
`DecalTexture<enum_RenderingServer_DecalTexture>`, texture:
`RID<class_RID>`) `🔗<class_RenderingServer_method_decal_set_texture>`

Sets the `texture` in the given texture `type` slot for the specified
decal. Equivalent to
`Decal.set_texture<class_Decal_method_set_texture>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **decals\_set\_filter**(filter:
`DecalFilter<enum_RenderingServer_DecalFilter>`)
`🔗<class_RenderingServer_method_decals_set_filter>`

Sets the texture `filter` mode to use when rendering decals. This
parameter is global and cannot be set on a per-decal basis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **directional\_light\_create**()
`🔗<class_RenderingServer_method_directional_light_create>`

Creates a directional light and adds it to the RenderingServer. It can
be accessed with the RID that is returned. This RID can be used in most
`light_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach this directional light to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

\*\*Note:\*\* The equivalent node is
`DirectionalLight3D<class_DirectionalLight3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**directional\_shadow\_atlas\_set\_size**(size: `int<class_int>`,
is\_16bits: `bool<class_bool>`)
`🔗<class_RenderingServer_method_directional_shadow_atlas_set_size>`

Sets the `size` of the directional light shadows in 3D. See also
`ProjectSettings.rendering/lights_and_shadows/directional_shadow/size<class_ProjectSettings_property_rendering/lights_and_shadows/directional_shadow/size>`.
This parameter is global and cannot be set on a per-viewport basis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**directional\_soft\_shadow\_filter\_set\_quality**(quality:
`ShadowQuality<enum_RenderingServer_ShadowQuality>`)
`🔗<class_RenderingServer_method_directional_soft_shadow_filter_set_quality>`

Sets the filter `quality` for directional light shadows in 3D. See also
`ProjectSettings.rendering/lights_and_shadows/directional_shadow/soft_shadow_filter_quality<class_ProjectSettings_property_rendering/lights_and_shadows/directional_shadow/soft_shadow_filter_quality>`.
This parameter is global and cannot be set on a per-viewport basis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **environment\_bake\_panorama**(environment:
`RID<class_RID>`, bake\_irradiance: `bool<class_bool>`, size:
`Vector2i<class_Vector2i>`)
`🔗<class_RenderingServer_method_environment_bake_panorama>`

Generates and returns an `Image<class_Image>` containing the radiance
map for the specified `environment` RID's sky. This supports built-in
sky material and custom sky shaders. If `bake_irradiance` is `true`, the
irradiance map is saved instead of the radiance map. The radiance map is
used to render reflected light, while the irradiance map is used to
render ambient light. See also
`sky_bake_panorama<class_RenderingServer_method_sky_bake_panorama>`.

\*\*Note:\*\* The image is saved in linear color space without any
tonemapping performed, which means it will look too dark if viewed
directly in an image editor.

\*\*Note:\*\* `size` should be a 2:1 aspect ratio for the generated
panorama to have square pixels. For radiance maps, there is no point in
using a height greater than
`Sky.radiance_size<class_Sky_property_radiance_size>`, as it won't
increase detail. Irradiance maps only contain low-frequency data, so
there is usually no point in going past a size of 128×64 pixels when
saving an irradiance map.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **environment\_create**()
`🔗<class_RenderingServer_method_environment_create>`

Creates an environment and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`environment_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is
`Environment<class_Environment>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**environment\_glow\_set\_use\_bicubic\_upscale**(enable:
`bool<class_bool>`)
`🔗<class_RenderingServer_method_environment_glow_set_use_bicubic_upscale>`

If `enable` is `true`, enables bicubic upscaling for glow which improves
quality at the cost of performance. Equivalent to
`ProjectSettings.rendering/environment/glow/upscale_mode<class_ProjectSettings_property_rendering/environment/glow/upscale_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_adjustment**(env:
`RID<class_RID>`, enable: `bool<class_bool>`, brightness:
`float<class_float>`, contrast: `float<class_float>`, saturation:
`float<class_float>`, use\_1d\_color\_correction: `bool<class_bool>`,
color\_correction: `RID<class_RID>`)
`🔗<class_RenderingServer_method_environment_set_adjustment>`

Sets the values to be used with the "adjustments" post-process effect.
See `Environment<class_Environment>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_ambient\_light**(env:
`RID<class_RID>`, color: `Color<class_Color>`, ambient:
`EnvironmentAmbientSource<enum_RenderingServer_EnvironmentAmbientSource>`
= 0, energy: `float<class_float>` = 1.0, sky\_contibution:
`float<class_float>` = 0.0, reflection\_source:
`EnvironmentReflectionSource<enum_RenderingServer_EnvironmentReflectionSource>`
= 0) `🔗<class_RenderingServer_method_environment_set_ambient_light>`

Sets the values to be used for ambient light rendering. See
`Environment<class_Environment>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_background**(env:
`RID<class_RID>`, bg:
`EnvironmentBG<enum_RenderingServer_EnvironmentBG>`)
`🔗<class_RenderingServer_method_environment_set_background>`

Sets the environment's background mode. Equivalent to
`Environment.background_mode<class_Environment_property_background_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_bg\_color**(env:
`RID<class_RID>`, color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_environment_set_bg_color>`

Color displayed for clear areas of the scene. Only effective if using
the `ENV_BG_COLOR<class_RenderingServer_constant_ENV_BG_COLOR>`
background mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_bg\_energy**(env:
`RID<class_RID>`, multiplier: `float<class_float>`, exposure\_value:
`float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_bg_energy>`

Sets the intensity of the background color.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_canvas\_max\_layer**(env:
`RID<class_RID>`, max\_layer: `int<class_int>`)
`🔗<class_RenderingServer_method_environment_set_canvas_max_layer>`

Sets the maximum layer to use if using Canvas background mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_fog**(env:
`RID<class_RID>`, enable: `bool<class_bool>`, light\_color:
`Color<class_Color>`, light\_energy: `float<class_float>`, sun\_scatter:
`float<class_float>`, density: `float<class_float>`, height:
`float<class_float>`, height\_density: `float<class_float>`,
aerial\_perspective: `float<class_float>`, sky\_affect:
`float<class_float>`, fog\_mode:
`EnvironmentFogMode<enum_RenderingServer_EnvironmentFogMode>` = 0)
`🔗<class_RenderingServer_method_environment_set_fog>`

Configures fog for the specified environment RID. See `fog_*` properties
in `Environment<class_Environment>` for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_glow**(env:
`RID<class_RID>`, enable: `bool<class_bool>`, levels:
`PackedFloat32Array<class_PackedFloat32Array>`, intensity:
`float<class_float>`, strength: `float<class_float>`, mix:
`float<class_float>`, bloom\_threshold: `float<class_float>`,
blend\_mode:
`EnvironmentGlowBlendMode<enum_RenderingServer_EnvironmentGlowBlendMode>`,
hdr\_bleed\_threshold: `float<class_float>`, hdr\_bleed\_scale:
`float<class_float>`, hdr\_luminance\_cap: `float<class_float>`,
glow\_map\_strength: `float<class_float>`, glow\_map: `RID<class_RID>`)
`🔗<class_RenderingServer_method_environment_set_glow>`

Configures glow for the specified environment RID. See `glow_*`
properties in `Environment<class_Environment>` for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_sdfgi**(env:
`RID<class_RID>`, enable: `bool<class_bool>`, cascades:
`int<class_int>`, min\_cell\_size: `float<class_float>`, y\_scale:
`EnvironmentSDFGIYScale<enum_RenderingServer_EnvironmentSDFGIYScale>`,
use\_occlusion: `bool<class_bool>`, bounce\_feedback:
`float<class_float>`, read\_sky: `bool<class_bool>`, energy:
`float<class_float>`, normal\_bias: `float<class_float>`, probe\_bias:
`float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_sdfgi>`

Configures signed distance field global illumination for the specified
environment RID. See `sdfgi_*` properties in
`Environment<class_Environment>` for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**environment\_set\_sdfgi\_frames\_to\_converge**(frames:
`EnvironmentSDFGIFramesToConverge<enum_RenderingServer_EnvironmentSDFGIFramesToConverge>`)
`🔗<class_RenderingServer_method_environment_set_sdfgi_frames_to_converge>`

Sets the number of frames to use for converging signed distance field
global illumination. Equivalent to
`ProjectSettings.rendering/global_illumination/sdfgi/frames_to_converge<class_ProjectSettings_property_rendering/global_illumination/sdfgi/frames_to_converge>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**environment\_set\_sdfgi\_frames\_to\_update\_light**(frames:
`EnvironmentSDFGIFramesToUpdateLight<enum_RenderingServer_EnvironmentSDFGIFramesToUpdateLight>`)
`🔗<class_RenderingServer_method_environment_set_sdfgi_frames_to_update_light>`

Sets the update speed for dynamic lights' indirect lighting when
computing signed distance field global illumination. Equivalent to
`ProjectSettings.rendering/global_illumination/sdfgi/frames_to_update_lights<class_ProjectSettings_property_rendering/global_illumination/sdfgi/frames_to_update_lights>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**environment\_set\_sdfgi\_ray\_count**(ray\_count:
`EnvironmentSDFGIRayCount<enum_RenderingServer_EnvironmentSDFGIRayCount>`)
`🔗<class_RenderingServer_method_environment_set_sdfgi_ray_count>`

Sets the number of rays to throw per frame when computing signed
distance field global illumination. Equivalent to
`ProjectSettings.rendering/global_illumination/sdfgi/probe_ray_count<class_ProjectSettings_property_rendering/global_illumination/sdfgi/probe_ray_count>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_sky**(env:
`RID<class_RID>`, sky: `RID<class_RID>`)
`🔗<class_RenderingServer_method_environment_set_sky>`

Sets the `Sky<class_Sky>` to be used as the environment's background
when using *BGMode* sky. Equivalent to
`Environment.sky<class_Environment_property_sky>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_sky\_custom\_fov**(env:
`RID<class_RID>`, scale: `float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_sky_custom_fov>`

Sets a custom field of view for the background `Sky<class_Sky>`.
Equivalent to
`Environment.sky_custom_fov<class_Environment_property_sky_custom_fov>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_sky\_orientation**(env:
`RID<class_RID>`, orientation: `Basis<class_Basis>`)
`🔗<class_RenderingServer_method_environment_set_sky_orientation>`

Sets the rotation of the background `Sky<class_Sky>` expressed as a
`Basis<class_Basis>`. Equivalent to
`Environment.sky_rotation<class_Environment_property_sky_rotation>`,
where the rotation vector is used to construct the `Basis<class_Basis>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_ssao**(env:
`RID<class_RID>`, enable: `bool<class_bool>`, radius:
`float<class_float>`, intensity: `float<class_float>`, power:
`float<class_float>`, detail: `float<class_float>`, horizon:
`float<class_float>`, sharpness: `float<class_float>`, light\_affect:
`float<class_float>`, ao\_channel\_affect: `float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_ssao>`

Sets the variables to be used with the screen-space ambient occlusion
(SSAO) post-process effect. See `Environment<class_Environment>` for
more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_ssao\_quality**(quality:
`EnvironmentSSAOQuality<enum_RenderingServer_EnvironmentSSAOQuality>`,
half\_size: `bool<class_bool>`, adaptive\_target: `float<class_float>`,
blur\_passes: `int<class_int>`, fadeout\_from: `float<class_float>`,
fadeout\_to: `float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_ssao_quality>`

Sets the quality level of the screen-space ambient occlusion (SSAO)
post-process effect. See `Environment<class_Environment>` for more
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_ssil\_quality**(quality:
`EnvironmentSSILQuality<enum_RenderingServer_EnvironmentSSILQuality>`,
half\_size: `bool<class_bool>`, adaptive\_target: `float<class_float>`,
blur\_passes: `int<class_int>`, fadeout\_from: `float<class_float>`,
fadeout\_to: `float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_ssil_quality>`

Sets the quality level of the screen-space indirect lighting (SSIL)
post-process effect. See `Environment<class_Environment>` for more
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_ssr**(env:
`RID<class_RID>`, enable: `bool<class_bool>`, max\_steps:
`int<class_int>`, fade\_in: `float<class_float>`, fade\_out:
`float<class_float>`, depth\_tolerance: `float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_ssr>`

Sets the variables to be used with the screen-space reflections (SSR)
post-process effect. See `Environment<class_Environment>` for more
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**environment\_set\_ssr\_roughness\_quality**(quality:
`EnvironmentSSRRoughnessQuality<enum_RenderingServer_EnvironmentSSRRoughnessQuality>`)
`🔗<class_RenderingServer_method_environment_set_ssr_roughness_quality>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_tonemap**(env:
`RID<class_RID>`, tone\_mapper:
`EnvironmentToneMapper<enum_RenderingServer_EnvironmentToneMapper>`,
exposure: `float<class_float>`, white: `float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_tonemap>`

Sets the variables to be used with the "tonemap" post-process effect.
See `Environment<class_Environment>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **environment\_set\_volumetric\_fog**(env:
`RID<class_RID>`, enable: `bool<class_bool>`, density:
`float<class_float>`, albedo: `Color<class_Color>`, emission:
`Color<class_Color>`, emission\_energy: `float<class_float>`,
anisotropy: `float<class_float>`, length: `float<class_float>`,
p\_detail\_spread: `float<class_float>`, gi\_inject:
`float<class_float>`, temporal\_reprojection: `bool<class_bool>`,
temporal\_reprojection\_amount: `float<class_float>`, ambient\_inject:
`float<class_float>`, sky\_affect: `float<class_float>`)
`🔗<class_RenderingServer_method_environment_set_volumetric_fog>`

Sets the variables to be used with the volumetric fog post-process
effect. See `Environment<class_Environment>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**environment\_set\_volumetric\_fog\_filter\_active**(active:
`bool<class_bool>`)
`🔗<class_RenderingServer_method_environment_set_volumetric_fog_filter_active>`

Enables filtering of the volumetric fog scattering buffer. This results
in much smoother volumes with very few under-sampling artifacts.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**environment\_set\_volumetric\_fog\_volume\_size**(size:
`int<class_int>`, depth: `int<class_int>`)
`🔗<class_RenderingServer_method_environment_set_volumetric_fog_volume_size>`

Sets the resolution of the volumetric fog's froxel buffer. `size` is
modified by the screen's aspect ratio and then used to set the width and
height of the buffer. While `depth` is directly used to set the depth of
the buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **fog\_volume\_create**()
`🔗<class_RenderingServer_method_fog_volume_create>`

Creates a new fog volume and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`fog_volume_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent node is `FogVolume<class_FogVolume>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fog\_volume\_set\_material**(fog\_volume:
`RID<class_RID>`, material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_fog_volume_set_material>`

Sets the `Material<class_Material>` of the fog volume. Can be either a
`FogMaterial<class_FogMaterial>` or a custom
`ShaderMaterial<class_ShaderMaterial>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fog\_volume\_set\_shape**(fog\_volume:
`RID<class_RID>`, shape:
`FogVolumeShape<enum_RenderingServer_FogVolumeShape>`)
`🔗<class_RenderingServer_method_fog_volume_set_shape>`

Sets the shape of the fog volume to either
`FOG_VOLUME_SHAPE_ELLIPSOID<class_RenderingServer_constant_FOG_VOLUME_SHAPE_ELLIPSOID>`,
`FOG_VOLUME_SHAPE_CONE<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CONE>`,
`FOG_VOLUME_SHAPE_CYLINDER<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CYLINDER>`,
`FOG_VOLUME_SHAPE_BOX<class_RenderingServer_constant_FOG_VOLUME_SHAPE_BOX>`
or
`FOG_VOLUME_SHAPE_WORLD<class_RenderingServer_constant_FOG_VOLUME_SHAPE_WORLD>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fog\_volume\_set\_size**(fog\_volume:
`RID<class_RID>`, size: `Vector3<class_Vector3>`)
`🔗<class_RenderingServer_method_fog_volume_set_size>`

Sets the size of the fog volume when shape is
`FOG_VOLUME_SHAPE_ELLIPSOID<class_RenderingServer_constant_FOG_VOLUME_SHAPE_ELLIPSOID>`,
`FOG_VOLUME_SHAPE_CONE<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CONE>`,
`FOG_VOLUME_SHAPE_CYLINDER<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CYLINDER>`
or
`FOG_VOLUME_SHAPE_BOX<class_RenderingServer_constant_FOG_VOLUME_SHAPE_BOX>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_draw**(swap\_buffers:
`bool<class_bool>` = true, frame\_step: `float<class_float>` = 0.0)
`🔗<class_RenderingServer_method_force_draw>`

Forces redrawing of all viewports at once. Must be called from the main
thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_sync**()
`🔗<class_RenderingServer_method_force_sync>`

Forces a synchronization between the CPU and GPU, which may be required
in certain cases. Only call this when needed, as CPU-GPU synchronization
has a performance cost.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **free\_rid**(rid: `RID<class_RID>`)
`🔗<class_RenderingServer_method_free_rid>`

Tries to free an object in the RenderingServer. To avoid memory leaks,
this should be called after using an object as memory management does
not occur automatically when using RenderingServer directly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_default\_clear\_color**()
`🔗<class_RenderingServer_method_get_default_clear_color>`

Returns the default clear color which is used when a specific clear
color has not been selected. See also
`set_default_clear_color<class_RenderingServer_method_set_default_clear_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_frame\_setup\_time\_cpu**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_get_frame_setup_time_cpu>`

Returns the time taken to setup rendering on the CPU in milliseconds.
This value is shared across all viewports and does *not* require
`viewport_set_measure_render_time<class_RenderingServer_method_viewport_set_measure_render_time>`
to be enabled on a viewport to be queried. See also
`viewport_get_measured_render_time_cpu<class_RenderingServer_method_viewport_get_measured_render_time_cpu>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RenderingDevice<class_RenderingDevice>` **get\_rendering\_device**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_get_rendering_device>`

Returns the global RenderingDevice.

\*\*Note:\*\* When using the OpenGL backend or when running in headless
mode, this function always returns `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_rendering\_info**(info:
`RenderingInfo<enum_RenderingServer_RenderingInfo>`)
`🔗<class_RenderingServer_method_get_rendering_info>`

Returns a statistic about the rendering engine which can be used for
performance profiling. See
`RenderingInfo<enum_RenderingServer_RenderingInfo>` for a list of values
that can be queried. See also
`viewport_get_render_info<class_RenderingServer_method_viewport_get_render_info>`,
which returns information specific to a viewport.

\*\*Note:\*\* Only 3D rendering is currently taken into account by some
of these values, such as the number of draw calls.

\*\*Note:\*\* Rendering information is not available until at least 2
frames have been rendered by the engine. If rendering information is not
available,
`get_rendering_info<class_RenderingServer_method_get_rendering_info>`
returns `0`. To print rendering information in `_ready()` successfully,
use the following:

    func _ready():
        for _i in 2:
            await get_tree().process_frame

        print(RenderingServer.get_rendering_info(RENDERING_INFO_TOTAL_DRAW_CALLS_IN_FRAME))

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_shader\_parameter\_list**(shader: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_get_shader_parameter_list>`

Returns the parameters of a shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_test\_cube**()
`🔗<class_RenderingServer_method_get_test_cube>`

Returns the RID of the test cube. This mesh will be created and returned
on the first call to
`get_test_cube<class_RenderingServer_method_get_test_cube>`, then it
will be cached for subsequent calls. See also
`make_sphere_mesh<class_RenderingServer_method_make_sphere_mesh>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_test\_texture**()
`🔗<class_RenderingServer_method_get_test_texture>`

Returns the RID of a 256×256 texture with a testing pattern on it (in
`Image.FORMAT_RGB8<class_Image_constant_FORMAT_RGB8>` format). This
texture will be created and returned on the first call to
`get_test_texture<class_RenderingServer_method_get_test_texture>`, then
it will be cached for subsequent calls. See also
`get_white_texture<class_RenderingServer_method_get_white_texture>`.

Example of getting the test texture and applying it to a
`Sprite2D<class_Sprite2D>` node:

    var texture_rid = RenderingServer.get_test_texture()
    var texture = ImageTexture.create_from_image(RenderingServer.texture_2d_get(texture_rid))
    $Sprite2D.texture = texture

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_video\_adapter\_api\_version**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_get_video_adapter_api_version>`

Returns the version of the graphics video adapter *currently in use*
(e.g. "1.2.189" for Vulkan, "3.3.0 NVIDIA 510.60.02" for OpenGL). This
version may be different from the actual latest version supported by the
hardware, as Godot may not always request the latest version. See also
`OS.get_video_adapter_driver_info<class_OS_method_get_video_adapter_driver_info>`.

\*\*Note:\*\* When running a headless or server binary, this function
returns an empty string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_video\_adapter\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_get_video_adapter_name>`

Returns the name of the video adapter (e.g. "GeForce GTX
1080/PCIe/SSE2").

\*\*Note:\*\* When running a headless or server binary, this function
returns an empty string.

\*\*Note:\*\* On the web platform, some browsers such as Firefox may
report a different, fixed GPU name such as "GeForce GTX 980" (regardless
of the user's actual GPU model). This is done to make fingerprinting
more difficult.

classref-item-separator

------------------------------------------------------------------------

classref-method

`DeviceType<enum_RenderingDevice_DeviceType>`
**get\_video\_adapter\_type**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_get_video_adapter_type>`

Returns the type of the video adapter. Since dedicated graphics cards
from a given generation will *usually* be significantly faster than
integrated graphics made in the same generation, the device type can be
used as a basis for automatic graphics settings adjustment. However,
this is not always true, so make sure to provide users with a way to
manually override graphics settings.

\*\*Note:\*\* When using the OpenGL backend or when running in headless
mode, this function always returns
`RenderingDevice.DEVICE_TYPE_OTHER<class_RenderingDevice_constant_DEVICE_TYPE_OTHER>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_video\_adapter\_vendor**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_get_video_adapter_vendor>`

Returns the vendor of the video adapter (e.g. "NVIDIA Corporation").

\*\*Note:\*\* When running a headless or server binary, this function
returns an empty string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_white\_texture**()
`🔗<class_RenderingServer_method_get_white_texture>`

Returns the ID of a 4×4 white texture (in
`Image.FORMAT_RGB8<class_Image_constant_FORMAT_RGB8>` format). This
texture will be created and returned on the first call to
`get_white_texture<class_RenderingServer_method_get_white_texture>`,
then it will be cached for subsequent calls. See also
`get_test_texture<class_RenderingServer_method_get_test_texture>`.

Example of getting the white texture and applying it to a
`Sprite2D<class_Sprite2D>` node:

    var texture_rid = RenderingServer.get_white_texture()
    var texture = ImageTexture.create_from_image(RenderingServer.texture_2d_get(texture_rid))
    $Sprite2D.texture = texture

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**gi\_set\_use\_half\_resolution**(half\_resolution: `bool<class_bool>`)
`🔗<class_RenderingServer_method_gi_set_use_half_resolution>`

If `half_resolution` is `true`, renders `VoxelGI<class_VoxelGI>` and
SDFGI
(`Environment.sdfgi_enabled<class_Environment_property_sdfgi_enabled>`)
buffers at halved resolution on each axis (e.g. 960×540 when the
viewport size is 1920×1080). This improves performance significantly
when VoxelGI or SDFGI is enabled, at the cost of artifacts that may be
visible on polygon edges. The loss in quality becomes less noticeable as
the viewport resolution increases. `LightmapGI<class_LightmapGI>`
rendering is not affected by this setting. Equivalent to
`ProjectSettings.rendering/global_illumination/gi/use_half_resolution<class_ProjectSettings_property_rendering/global_illumination/gi/use_half_resolution>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_shader\_parameter\_add**(name:
`StringName<class_StringName>`, type:
`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`,
default\_value: `Variant<class_Variant>`)
`🔗<class_RenderingServer_method_global_shader_parameter_add>`

Creates a new global shader uniform.

\*\*Note:\*\* Global shader parameter names are case-sensitive.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **global\_shader\_parameter\_get**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_global_shader_parameter_get>`

Returns the value of the global shader uniform specified by `name`.

\*\*Note:\*\*
`global_shader_parameter_get<class_RenderingServer_method_global_shader_parameter_get>`
has a large performance penalty as the rendering thread needs to
synchronize with the calling thread, which is slow. Do not use this
method during gameplay to avoid stuttering. If you need to read values
in a script after setting them, consider creating an autoload where you
store the values you need to query at the same time you're setting them
as global parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\]
**global\_shader\_parameter\_get\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_global_shader_parameter_get_list>`

Returns the list of global shader uniform names.

\*\*Note:\*\*
`global_shader_parameter_get<class_RenderingServer_method_global_shader_parameter_get>`
has a large performance penalty as the rendering thread needs to
synchronize with the calling thread, which is slow. Do not use this
method during gameplay to avoid stuttering. If you need to read values
in a script after setting them, consider creating an autoload where you
store the values you need to query at the same time you're setting them
as global parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GlobalShaderParameterType<enum_RenderingServer_GlobalShaderParameterType>`
**global\_shader\_parameter\_get\_type**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_global_shader_parameter_get_type>`

Returns the type associated to the global shader uniform specified by
`name`.

\*\*Note:\*\*
`global_shader_parameter_get<class_RenderingServer_method_global_shader_parameter_get>`
has a large performance penalty as the rendering thread needs to
synchronize with the calling thread, which is slow. Do not use this
method during gameplay to avoid stuttering. If you need to read values
in a script after setting them, consider creating an autoload where you
store the values you need to query at the same time you're setting them
as global parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_shader\_parameter\_remove**(name:
`StringName<class_StringName>`)
`🔗<class_RenderingServer_method_global_shader_parameter_remove>`

Removes the global shader uniform specified by `name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_shader\_parameter\_set**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_RenderingServer_method_global_shader_parameter_set>`

Sets the global shader uniform `name` to `value`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_shader\_parameter\_set\_override**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_RenderingServer_method_global_shader_parameter_set_override>`

Overrides the global shader uniform `name` with `value`. Equivalent to
the `ShaderGlobalsOverride<class_ShaderGlobalsOverride>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_changed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_has_changed>`

Returns `true` if changes have been made to the RenderingServer's data.
`force_draw<class_RenderingServer_method_force_draw>` is usually called
if this happens.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_feature**(feature:
`Features<enum_RenderingServer_Features>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_has_feature>`

**Deprecated:** This method has not been used since Godot 3.0.

This method does nothing and always returns `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_os\_feature**(feature: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_has_os_feature>`

Returns `true` if the OS supports a certain `feature`. Features might be
`s3tc`, `etc`, and `etc2`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_attach\_object\_instance\_id**(instance: `RID<class_RID>`,
id: `int<class_int>`)
`🔗<class_RenderingServer_method_instance_attach_object_instance_id>`

Attaches a unique Object ID to instance. Object ID must be attached to
instance for proper culling with
`instances_cull_aabb<class_RenderingServer_method_instances_cull_aabb>`,
`instances_cull_convex<class_RenderingServer_method_instances_cull_convex>`,
and
`instances_cull_ray<class_RenderingServer_method_instances_cull_ray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_attach\_skeleton**(instance:
`RID<class_RID>`, skeleton: `RID<class_RID>`)
`🔗<class_RenderingServer_method_instance_attach_skeleton>`

Attaches a skeleton to an instance. Removes the previous skeleton from
the instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **instance\_create**()
`🔗<class_RenderingServer_method_instance_create>`

Creates a visual instance and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`instance_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

An instance is a way of placing a 3D object in the scenario. Objects
like particles, meshes, reflection probes and decals need to be
associated with an instance to be visible in the scenario using
`instance_set_base<class_RenderingServer_method_instance_set_base>`.

\*\*Note:\*\* The equivalent node is
`VisualInstance3D<class_VisualInstance3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **instance\_create2**(base: `RID<class_RID>`, scenario:
`RID<class_RID>`) `🔗<class_RenderingServer_method_instance_create2>`

Creates a visual instance, adds it to the RenderingServer, and sets both
base and scenario. It can be accessed with the RID that is returned.
This RID will be used in all `instance_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method. This is a shorthand for using
`instance_create<class_RenderingServer_method_instance_create>` and
setting the base and scenario manually.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>`
**instance\_geometry\_get\_shader\_parameter**(instance:
`RID<class_RID>`, parameter: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_instance_geometry_get_shader_parameter>`

Returns the value of the per-instance shader uniform from the specified
3D geometry instance. Equivalent to
`GeometryInstance3D.get_instance_shader_parameter<class_GeometryInstance3D_method_get_instance_shader_parameter>`.

\*\*Note:\*\* Per-instance shader parameter names are case-sensitive.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>`
**instance\_geometry\_get\_shader\_parameter\_default\_value**(instance:
`RID<class_RID>`, parameter: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_instance_geometry_get_shader_parameter_default_value>`

Returns the default value of the per-instance shader uniform from the
specified 3D geometry instance. Equivalent to
`GeometryInstance3D.get_instance_shader_parameter<class_GeometryInstance3D_method_get_instance_shader_parameter>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**instance\_geometry\_get\_shader\_parameter\_list**(instance:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_instance_geometry_get_shader_parameter_list>`

Returns a dictionary of per-instance shader uniform names of the
per-instance shader uniform from the specified 3D geometry instance. The
returned dictionary is in PropertyInfo format, with the keys `name`,
`class_name`, `type`, `hint`, `hint_string` and `usage`. Equivalent to
`GeometryInstance3D.get_instance_shader_parameter<class_GeometryInstance3D_method_get_instance_shader_parameter>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_geometry\_set\_cast\_shadows\_setting**(instance:
`RID<class_RID>`, shadow\_casting\_setting:
`ShadowCastingSetting<enum_RenderingServer_ShadowCastingSetting>`)
`🔗<class_RenderingServer_method_instance_geometry_set_cast_shadows_setting>`

Sets the shadow casting setting to one of
`ShadowCastingSetting<enum_RenderingServer_ShadowCastingSetting>`.
Equivalent to
`GeometryInstance3D.cast_shadow<class_GeometryInstance3D_property_cast_shadow>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_geometry\_set\_flag**(instance:
`RID<class_RID>`, flag:
`InstanceFlags<enum_RenderingServer_InstanceFlags>`, enabled:
`bool<class_bool>`)
`🔗<class_RenderingServer_method_instance_geometry_set_flag>`

Sets the flag for a given
`InstanceFlags<enum_RenderingServer_InstanceFlags>`. See
`InstanceFlags<enum_RenderingServer_InstanceFlags>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_geometry\_set\_lightmap**(instance: `RID<class_RID>`,
lightmap: `RID<class_RID>`, lightmap\_uv\_scale: `Rect2<class_Rect2>`,
lightmap\_slice: `int<class_int>`)
`🔗<class_RenderingServer_method_instance_geometry_set_lightmap>`

Sets the lightmap GI instance to use for the specified 3D geometry
instance. The lightmap UV scale for the specified instance (equivalent
to
`GeometryInstance3D.gi_lightmap_scale<class_GeometryInstance3D_property_gi_lightmap_scale>`)
and lightmap atlas slice must also be specified.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_geometry\_set\_lod\_bias**(instance: `RID<class_RID>`,
lod\_bias: `float<class_float>`)
`🔗<class_RenderingServer_method_instance_geometry_set_lod_bias>`

Sets the level of detail bias to use when rendering the specified 3D
geometry instance. Higher values result in higher detail from further
away. Equivalent to
`GeometryInstance3D.lod_bias<class_GeometryInstance3D_property_lod_bias>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_geometry\_set\_material\_overlay**(instance:
`RID<class_RID>`, material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_instance_geometry_set_material_overlay>`

Sets a material that will be rendered for all surfaces on top of active
materials for the mesh associated with this instance. Equivalent to
`GeometryInstance3D.material_overlay<class_GeometryInstance3D_property_material_overlay>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_geometry\_set\_material\_override**(instance:
`RID<class_RID>`, material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_instance_geometry_set_material_override>`

Sets a material that will override the material for all surfaces on the
mesh associated with this instance. Equivalent to
`GeometryInstance3D.material_override<class_GeometryInstance3D_property_material_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_geometry\_set\_shader\_parameter**(instance:
`RID<class_RID>`, parameter: `StringName<class_StringName>`, value:
`Variant<class_Variant>`)
`🔗<class_RenderingServer_method_instance_geometry_set_shader_parameter>`

Sets the per-instance shader uniform on the specified 3D geometry
instance. Equivalent to
`GeometryInstance3D.set_instance_shader_parameter<class_GeometryInstance3D_method_set_instance_shader_parameter>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_geometry\_set\_transparency**(instance: `RID<class_RID>`,
transparency: `float<class_float>`)
`🔗<class_RenderingServer_method_instance_geometry_set_transparency>`

Sets the transparency for the given geometry instance. Equivalent to
`GeometryInstance3D.transparency<class_GeometryInstance3D_property_transparency>`.

A transparency of `0.0` is fully opaque, while `1.0` is fully
transparent. Values greater than `0.0` (exclusive) will force the
geometry's materials to go through the transparent pipeline, which is
slower to render and can exhibit rendering issues due to incorrect
transparency sorting. However, unlike using a transparent material,
setting `transparency` to a value greater than `0.0` (exclusive) will
*not* disable shadow rendering.

In spatial shaders, `1.0 - transparency` is set as the default value of
the `ALPHA` built-in.

\*\*Note:\*\* `transparency` is clamped between `0.0` and `1.0`, so this
property cannot be used to make transparent materials more opaque than
they originally are.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_geometry\_set\_visibility\_range**(instance:
`RID<class_RID>`, min: `float<class_float>`, max: `float<class_float>`,
min\_margin: `float<class_float>`, max\_margin: `float<class_float>`,
fade\_mode:
`VisibilityRangeFadeMode<enum_RenderingServer_VisibilityRangeFadeMode>`)
`🔗<class_RenderingServer_method_instance_geometry_set_visibility_range>`

Sets the visibility range values for the given geometry instance.
Equivalent to
`GeometryInstance3D.visibility_range_begin<class_GeometryInstance3D_property_visibility_range_begin>`
and related properties.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_reset\_physics\_interpolation**(instance: `RID<class_RID>`)
`🔗<class_RenderingServer_method_instance_reset_physics_interpolation>`

Prevents physics interpolation for the current physics tick.

This is useful when moving an instance to a new location, to give an
instantaneous change rather than interpolation from the previous
location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_base**(instance:
`RID<class_RID>`, base: `RID<class_RID>`)
`🔗<class_RenderingServer_method_instance_set_base>`

Sets the base of the instance. A base can be any of the 3D objects that
are created in the RenderingServer that can be displayed. For example,
any of the light types, mesh, multimesh, particle system, reflection
probe, decal, lightmap, voxel GI and visibility notifiers are all types
that can be set as the base of an instance in order to be displayed in
the scenario.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_set\_blend\_shape\_weight**(instance: `RID<class_RID>`,
shape: `int<class_int>`, weight: `float<class_float>`)
`🔗<class_RenderingServer_method_instance_set_blend_shape_weight>`

Sets the weight for a given blend shape associated with this instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_custom\_aabb**(instance:
`RID<class_RID>`, aabb: `AABB<class_AABB>`)
`🔗<class_RenderingServer_method_instance_set_custom_aabb>`

Sets a custom AABB to use when culling objects from the view frustum.
Equivalent to setting
`GeometryInstance3D.custom_aabb<class_GeometryInstance3D_property_custom_aabb>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_set\_extra\_visibility\_margin**(instance: `RID<class_RID>`,
margin: `float<class_float>`)
`🔗<class_RenderingServer_method_instance_set_extra_visibility_margin>`

Sets a margin to increase the size of the AABB when culling objects from
the view frustum. This allows you to avoid culling objects that fall
outside the view frustum. Equivalent to
`GeometryInstance3D.extra_cull_margin<class_GeometryInstance3D_property_extra_cull_margin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_ignore\_culling**(instance:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_instance_set_ignore_culling>`

If `true`, ignores both frustum and occlusion culling on the specified
3D geometry instance. This is not the same as
`GeometryInstance3D.ignore_occlusion_culling<class_GeometryInstance3D_property_ignore_occlusion_culling>`,
which only ignores occlusion culling and leaves frustum culling intact.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_interpolated**(instance:
`RID<class_RID>`, interpolated: `bool<class_bool>`)
`🔗<class_RenderingServer_method_instance_set_interpolated>`

Turns on and off physics interpolation for the instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_layer\_mask**(instance:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_RenderingServer_method_instance_set_layer_mask>`

Sets the render layers that this instance will be drawn to. Equivalent
to `VisualInstance3D.layers<class_VisualInstance3D_property_layers>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_pivot\_data**(instance:
`RID<class_RID>`, sorting\_offset: `float<class_float>`,
use\_aabb\_center: `bool<class_bool>`)
`🔗<class_RenderingServer_method_instance_set_pivot_data>`

Sets the sorting offset and switches between using the bounding box or
instance origin for depth sorting.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_scenario**(instance:
`RID<class_RID>`, scenario: `RID<class_RID>`)
`🔗<class_RenderingServer_method_instance_set_scenario>`

Sets the scenario that the instance is in. The scenario is the 3D world
that the objects will be displayed in.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_set\_surface\_override\_material**(instance:
`RID<class_RID>`, surface: `int<class_int>`, material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_instance_set_surface_override_material>`

Sets the override material of a specific surface. Equivalent to
`MeshInstance3D.set_surface_override_material<class_MeshInstance3D_method_set_surface_override_material>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_transform**(instance:
`RID<class_RID>`, transform: `Transform3D<class_Transform3D>`)
`🔗<class_RenderingServer_method_instance_set_transform>`

Sets the world space transform of the instance. Equivalent to
`Node3D.global_transform<class_Node3D_property_global_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**instance\_set\_visibility\_parent**(instance: `RID<class_RID>`,
parent: `RID<class_RID>`)
`🔗<class_RenderingServer_method_instance_set_visibility_parent>`

Sets the visibility parent for the given instance. Equivalent to
`Node3D.visibility_parent<class_Node3D_property_visibility_parent>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **instance\_set\_visible**(instance:
`RID<class_RID>`, visible: `bool<class_bool>`)
`🔗<class_RenderingServer_method_instance_set_visible>`

Sets whether an instance is drawn or not. Equivalent to
`Node3D.visible<class_Node3D_property_visible>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>`
**instances\_cull\_aabb**(aabb: `AABB<class_AABB>`, scenario:
`RID<class_RID>` = RID())
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_instances_cull_aabb>`

Returns an array of object IDs intersecting with the provided AABB. Only
3D nodes that inherit from `VisualInstance3D<class_VisualInstance3D>`
are considered, such as `MeshInstance3D<class_MeshInstance3D>` or
`DirectionalLight3D<class_DirectionalLight3D>`. Use
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`
to obtain the actual nodes. A scenario RID must be provided, which is
available in the `World3D<class_World3D>` you want to query. This forces
an update for all resources queued to update.

\*\*Warning:\*\* This function is primarily intended for editor usage.
For in-game use cases, prefer physics collision.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>`
**instances\_cull\_convex**(convex:
`Array<class_Array>`\[`Plane<class_Plane>`\], scenario: `RID<class_RID>`
= RID())
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_instances_cull_convex>`

Returns an array of object IDs intersecting with the provided convex
shape. Only 3D nodes that inherit from
`VisualInstance3D<class_VisualInstance3D>` are considered, such as
`MeshInstance3D<class_MeshInstance3D>` or
`DirectionalLight3D<class_DirectionalLight3D>`. Use
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`
to obtain the actual nodes. A scenario RID must be provided, which is
available in the `World3D<class_World3D>` you want to query. This forces
an update for all resources queued to update.

\*\*Warning:\*\* This function is primarily intended for editor usage.
For in-game use cases, prefer physics collision.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>`
**instances\_cull\_ray**(from: `Vector3<class_Vector3>`, to:
`Vector3<class_Vector3>`, scenario: `RID<class_RID>` = RID())
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_instances_cull_ray>`

Returns an array of object IDs intersecting with the provided 3D ray.
Only 3D nodes that inherit from
`VisualInstance3D<class_VisualInstance3D>` are considered, such as
`MeshInstance3D<class_MeshInstance3D>` or
`DirectionalLight3D<class_DirectionalLight3D>`. Use
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`
to obtain the actual nodes. A scenario RID must be provided, which is
available in the `World3D<class_World3D>` you want to query. This forces
an update for all resources queued to update.

\*\*Warning:\*\* This function is primarily intended for editor usage.
For in-game use cases, prefer physics collision.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_on\_render\_thread**()
`🔗<class_RenderingServer_method_is_on_render_thread>`

Returns `true` if our code is currently executing on the rendering
thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**light\_directional\_set\_blend\_splits**(light: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_light_directional_set_blend_splits>`

If `true`, this directional light will blend between shadow map splits
resulting in a smoother transition between them. Equivalent to
`DirectionalLight3D.directional_shadow_blend_splits<class_DirectionalLight3D_property_directional_shadow_blend_splits>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**light\_directional\_set\_shadow\_mode**(light: `RID<class_RID>`, mode:
`LightDirectionalShadowMode<enum_RenderingServer_LightDirectionalShadowMode>`)
`🔗<class_RenderingServer_method_light_directional_set_shadow_mode>`

Sets the shadow mode for this directional light. Equivalent to
`DirectionalLight3D.directional_shadow_mode<class_DirectionalLight3D_property_directional_shadow_mode>`.
See
`LightDirectionalShadowMode<enum_RenderingServer_LightDirectionalShadowMode>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_directional\_set\_sky\_mode**(light:
`RID<class_RID>`, mode:
`LightDirectionalSkyMode<enum_RenderingServer_LightDirectionalSkyMode>`)
`🔗<class_RenderingServer_method_light_directional_set_sky_mode>`

If `true`, this light will not be used for anything except sky shaders.
Use this for lights that impact your sky shader that you may want to
hide from affecting the rest of the scene. For example, you may want to
enable this when the sun in your sky shader falls below the horizon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_omni\_set\_shadow\_mode**(light:
`RID<class_RID>`, mode:
`LightOmniShadowMode<enum_RenderingServer_LightOmniShadowMode>`)
`🔗<class_RenderingServer_method_light_omni_set_shadow_mode>`

Sets whether to use a dual paraboloid or a cubemap for the shadow map.
Dual paraboloid is faster but may suffer from artifacts. Equivalent to
`OmniLight3D.omni_shadow_mode<class_OmniLight3D_property_omni_shadow_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_projectors\_set\_filter**(filter:
`LightProjectorFilter<enum_RenderingServer_LightProjectorFilter>`)
`🔗<class_RenderingServer_method_light_projectors_set_filter>`

Sets the texture filter mode to use when rendering light projectors.
This parameter is global and cannot be set on a per-light basis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_bake\_mode**(light:
`RID<class_RID>`, bake\_mode:
`LightBakeMode<enum_RenderingServer_LightBakeMode>`)
`🔗<class_RenderingServer_method_light_set_bake_mode>`

Sets the bake mode to use for the specified 3D light. Equivalent to
`Light3D.light_bake_mode<class_Light3D_property_light_bake_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_color**(light: `RID<class_RID>`,
color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_light_set_color>`

Sets the color of the light. Equivalent to
`Light3D.light_color<class_Light3D_property_light_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_cull\_mask**(light:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_RenderingServer_method_light_set_cull_mask>`

Sets the cull mask for this 3D light. Lights only affect objects in the
selected layers. Equivalent to
`Light3D.light_cull_mask<class_Light3D_property_light_cull_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_distance\_fade**(decal:
`RID<class_RID>`, enabled: `bool<class_bool>`, begin:
`float<class_float>`, shadow: `float<class_float>`, length:
`float<class_float>`)
`🔗<class_RenderingServer_method_light_set_distance_fade>`

Sets the distance fade for this 3D light. This acts as a form of level
of detail (LOD) and can be used to improve performance. Equivalent to
`Light3D.distance_fade_enabled<class_Light3D_property_distance_fade_enabled>`,
`Light3D.distance_fade_begin<class_Light3D_property_distance_fade_begin>`,
`Light3D.distance_fade_shadow<class_Light3D_property_distance_fade_shadow>`,
and
`Light3D.distance_fade_length<class_Light3D_property_distance_fade_length>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_max\_sdfgi\_cascade**(light:
`RID<class_RID>`, cascade: `int<class_int>`)
`🔗<class_RenderingServer_method_light_set_max_sdfgi_cascade>`

Sets the maximum SDFGI cascade in which the 3D light's indirect lighting
is rendered. Higher values allow the light to be rendered in SDFGI
further away from the camera.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_negative**(light:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_light_set_negative>`

If `true`, the 3D light will subtract light instead of adding light.
Equivalent to
`Light3D.light_negative<class_Light3D_property_light_negative>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_param**(light: `RID<class_RID>`,
param: `LightParam<enum_RenderingServer_LightParam>`, value:
`float<class_float>`) `🔗<class_RenderingServer_method_light_set_param>`

Sets the specified 3D light parameter. See
`LightParam<enum_RenderingServer_LightParam>` for options. Equivalent to
`Light3D.set_param<class_Light3D_method_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_projector**(light:
`RID<class_RID>`, texture: `RID<class_RID>`)
`🔗<class_RenderingServer_method_light_set_projector>`

Sets the projector texture to use for the specified 3D light. Equivalent
to `Light3D.light_projector<class_Light3D_property_light_projector>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**light\_set\_reverse\_cull\_face\_mode**(light: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_light_set_reverse_cull_face_mode>`

If `true`, reverses the backface culling of the mesh. This can be useful
when you have a flat mesh that has a light behind it. If you need to
cast a shadow on both sides of the mesh, set the mesh to use
double-sided shadows with
`instance_geometry_set_cast_shadows_setting<class_RenderingServer_method_instance_geometry_set_cast_shadows_setting>`.
Equivalent to
`Light3D.shadow_reverse_cull_face<class_Light3D_property_shadow_reverse_cull_face>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **light\_set\_shadow**(light:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_light_set_shadow>`

If `true`, light will cast shadows. Equivalent to
`Light3D.shadow_enabled<class_Light3D_property_shadow_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **lightmap\_create**()
`🔗<class_RenderingServer_method_lightmap_create>`

Creates a new lightmap global illumination instance and adds it to the
RenderingServer. It can be accessed with the RID that is returned. This
RID will be used in all `lightmap_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent node is `LightmapGI<class_LightmapGI>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**lightmap\_get\_probe\_capture\_bsp\_tree**(lightmap: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_lightmap_get_probe_capture_bsp_tree>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**lightmap\_get\_probe\_capture\_points**(lightmap: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_lightmap_get_probe_capture_points>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedColorArray<class_PackedColorArray>`
**lightmap\_get\_probe\_capture\_sh**(lightmap: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_lightmap_get_probe_capture_sh>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**lightmap\_get\_probe\_capture\_tetrahedra**(lightmap:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_lightmap_get_probe_capture_tetrahedra>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**lightmap\_set\_baked\_exposure\_normalization**(lightmap:
`RID<class_RID>`, baked\_exposure: `float<class_float>`)
`🔗<class_RenderingServer_method_lightmap_set_baked_exposure_normalization>`

Used to inform the renderer what exposure normalization value was used
while baking the lightmap. This value will be used and modulated at run
time to ensure that the lightmap maintains a consistent level of
exposure even if the scene-wide exposure normalization is changed at run
time. For more information see
`camera_attributes_set_exposure<class_RenderingServer_method_camera_attributes_set_exposure>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **lightmap\_set\_probe\_bounds**(lightmap:
`RID<class_RID>`, bounds: `AABB<class_AABB>`)
`🔗<class_RenderingServer_method_lightmap_set_probe_bounds>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**lightmap\_set\_probe\_capture\_data**(lightmap: `RID<class_RID>`,
points: `PackedVector3Array<class_PackedVector3Array>`, point\_sh:
`PackedColorArray<class_PackedColorArray>`, tetrahedra:
`PackedInt32Array<class_PackedInt32Array>`, bsp\_tree:
`PackedInt32Array<class_PackedInt32Array>`)
`🔗<class_RenderingServer_method_lightmap_set_probe_capture_data>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**lightmap\_set\_probe\_capture\_update\_speed**(speed:
`float<class_float>`)
`🔗<class_RenderingServer_method_lightmap_set_probe_capture_update_speed>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **lightmap\_set\_probe\_interior**(lightmap:
`RID<class_RID>`, interior: `bool<class_bool>`)
`🔗<class_RenderingServer_method_lightmap_set_probe_interior>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **lightmap\_set\_textures**(lightmap:
`RID<class_RID>`, light: `RID<class_RID>`, uses\_sh: `bool<class_bool>`)
`🔗<class_RenderingServer_method_lightmap_set_textures>`

Set the textures on the given `lightmap` GI instance to the texture
array pointed to by the `light` RID. If the lightmap texture was baked
with `LightmapGI.directional<class_LightmapGI_property_directional>` set
to `true`, then `uses_sh` must also be `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **lightmaps\_set\_bicubic\_filter**(enable:
`bool<class_bool>`)
`🔗<class_RenderingServer_method_lightmaps_set_bicubic_filter>`

Toggles whether a bicubic filter should be used when lightmaps are
sampled. This smoothens their appearance at a performance cost.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **make\_sphere\_mesh**(latitudes: `int<class_int>`,
longitudes: `int<class_int>`, radius: `float<class_float>`)
`🔗<class_RenderingServer_method_make_sphere_mesh>`

Returns a mesh of a sphere with the given number of horizontal
subdivisions, vertical subdivisions and radius. See also
`get_test_cube<class_RenderingServer_method_get_test_cube>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **material\_create**()
`🔗<class_RenderingServer_method_material_create>`

Creates an empty material and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`material_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is `Material<class_Material>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **material\_get\_param**(material:
`RID<class_RID>`, parameter: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_material_get_param>`

Returns the value of a certain material's parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **material\_set\_next\_pass**(material:
`RID<class_RID>`, next\_material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_material_set_next_pass>`

Sets an object's next material.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **material\_set\_param**(material:
`RID<class_RID>`, parameter: `StringName<class_StringName>`, value:
`Variant<class_Variant>`)
`🔗<class_RenderingServer_method_material_set_param>`

Sets a material's parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **material\_set\_render\_priority**(material:
`RID<class_RID>`, priority: `int<class_int>`)
`🔗<class_RenderingServer_method_material_set_render_priority>`

Sets a material's render priority.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **material\_set\_shader**(shader\_material:
`RID<class_RID>`, shader: `RID<class_RID>`)
`🔗<class_RenderingServer_method_material_set_shader>`

Sets a shader material's shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mesh\_add\_surface**(mesh: `RID<class_RID>`,
surface: `Dictionary<class_Dictionary>`)
`🔗<class_RenderingServer_method_mesh_add_surface>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mesh\_add\_surface\_from\_arrays**(mesh:
`RID<class_RID>`, primitive:
`PrimitiveType<enum_RenderingServer_PrimitiveType>`, arrays:
`Array<class_Array>`, blend\_shapes: `Array<class_Array>` = \[\], lods:
`Dictionary<class_Dictionary>` = {}, compress\_format:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ArrayFormat<enum_RenderingServer_ArrayFormat>`\]
= 0) `🔗<class_RenderingServer_method_mesh_add_surface_from_arrays>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mesh\_clear**(mesh: `RID<class_RID>`)
`🔗<class_RenderingServer_method_mesh_clear>`

Removes all surfaces from a mesh.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **mesh\_create**()
`🔗<class_RenderingServer_method_mesh_create>`

Creates a new mesh and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`mesh_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach this mesh to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

\*\*Note:\*\* The equivalent resource is `Mesh<class_Mesh>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **mesh\_create\_from\_surfaces**(surfaces:
`Array<class_Array>`\[`Dictionary<class_Dictionary>`\],
blend\_shape\_count: `int<class_int>` = 0)
`🔗<class_RenderingServer_method_mesh_create_from_surfaces>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **mesh\_get\_blend\_shape\_count**(mesh:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_get_blend_shape_count>`

Returns a mesh's blend shape count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BlendShapeMode<enum_RenderingServer_BlendShapeMode>`
**mesh\_get\_blend\_shape\_mode**(mesh: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_get_blend_shape_mode>`

Returns a mesh's blend shape mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AABB<class_AABB>` **mesh\_get\_custom\_aabb**(mesh: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_get_custom_aabb>`

Returns a mesh's custom aabb.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **mesh\_get\_surface**(mesh:
`RID<class_RID>`, surface: `int<class_int>`)
`🔗<class_RenderingServer_method_mesh_get_surface>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **mesh\_get\_surface\_count**(mesh: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_get_surface_count>`

Returns a mesh's number of surfaces.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mesh\_set\_blend\_shape\_mode**(mesh:
`RID<class_RID>`, mode:
`BlendShapeMode<enum_RenderingServer_BlendShapeMode>`)
`🔗<class_RenderingServer_method_mesh_set_blend_shape_mode>`

Sets a mesh's blend shape mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mesh\_set\_custom\_aabb**(mesh:
`RID<class_RID>`, aabb: `AABB<class_AABB>`)
`🔗<class_RenderingServer_method_mesh_set_custom_aabb>`

Sets a mesh's custom aabb.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mesh\_set\_shadow\_mesh**(mesh:
`RID<class_RID>`, shadow\_mesh: `RID<class_RID>`)
`🔗<class_RenderingServer_method_mesh_set_shadow_mesh>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **mesh\_surface\_get\_arrays**(mesh:
`RID<class_RID>`, surface: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_surface_get_arrays>`

Returns a mesh's surface's buffer arrays.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Array<class_Array>`\]
**mesh\_surface\_get\_blend\_shape\_arrays**(mesh: `RID<class_RID>`,
surface: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_surface_get_blend_shape_arrays>`

Returns a mesh's surface's arrays for blend shapes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**mesh\_surface\_get\_format\_attribute\_stride**(format:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ArrayFormat<enum_RenderingServer_ArrayFormat>`\],
vertex\_count: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_surface_get_format_attribute_stride>`

Returns the stride of the attribute buffer for a mesh with given
`format`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**mesh\_surface\_get\_format\_normal\_tangent\_stride**(format:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ArrayFormat<enum_RenderingServer_ArrayFormat>`\],
vertex\_count: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_surface_get_format_normal_tangent_stride>`

Returns the stride of the combined normals and tangents for a mesh with
given `format`. Note importantly that, while normals and tangents are in
the vertex buffer with vertices, they are only interleaved with each
other and so have a different stride than vertex positions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **mesh\_surface\_get\_format\_offset**(format:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ArrayFormat<enum_RenderingServer_ArrayFormat>`\],
vertex\_count: `int<class_int>`, array\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_surface_get_format_offset>`

Returns the offset of a given attribute by `array_index` in the start of
its respective buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **mesh\_surface\_get\_format\_skin\_stride**(format:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ArrayFormat<enum_RenderingServer_ArrayFormat>`\],
vertex\_count: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_surface_get_format_skin_stride>`

Returns the stride of the skin buffer for a mesh with given `format`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **mesh\_surface\_get\_format\_vertex\_stride**(format:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ArrayFormat<enum_RenderingServer_ArrayFormat>`\],
vertex\_count: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_surface_get_format_vertex_stride>`

Returns the stride of the vertex positions for a mesh with given
`format`. Note importantly that vertex positions are stored
consecutively and are not interleaved with the other attributes in the
vertex buffer (normals and tangents).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **mesh\_surface\_get\_material**(mesh:
`RID<class_RID>`, surface: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_mesh_surface_get_material>`

Returns a mesh's surface's material.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mesh\_surface\_set\_material**(mesh:
`RID<class_RID>`, surface: `int<class_int>`, material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_mesh_surface_set_material>`

Sets a mesh's surface's material.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**mesh\_surface\_update\_attribute\_region**(mesh: `RID<class_RID>`,
surface: `int<class_int>`, offset: `int<class_int>`, data:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_RenderingServer_method_mesh_surface_update_attribute_region>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mesh\_surface\_update\_skin\_region**(mesh:
`RID<class_RID>`, surface: `int<class_int>`, offset: `int<class_int>`,
data: `PackedByteArray<class_PackedByteArray>`)
`🔗<class_RenderingServer_method_mesh_surface_update_skin_region>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**mesh\_surface\_update\_vertex\_region**(mesh: `RID<class_RID>`,
surface: `int<class_int>`, offset: `int<class_int>`, data:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_RenderingServer_method_mesh_surface_update_vertex_region>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **multimesh\_allocate\_data**(multimesh:
`RID<class_RID>`, instances: `int<class_int>`, transform\_format:
`MultimeshTransformFormat<enum_RenderingServer_MultimeshTransformFormat>`,
color\_format: `bool<class_bool>` = false, custom\_data\_format:
`bool<class_bool>` = false)
`🔗<class_RenderingServer_method_multimesh_allocate_data>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **multimesh\_create**()
`🔗<class_RenderingServer_method_multimesh_create>`

Creates a new multimesh on the RenderingServer and returns an
`RID<class_RID>` handle. This RID will be used in all `multimesh_*`
RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach this multimesh to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

\*\*Note:\*\* The equivalent resource is `MultiMesh<class_MultiMesh>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AABB<class_AABB>` **multimesh\_get\_aabb**(multimesh: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_get_aabb>`

Calculates and returns the axis-aligned bounding box that encloses all
instances within the multimesh.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedFloat32Array<class_PackedFloat32Array>`
**multimesh\_get\_buffer**(multimesh: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_get_buffer>`

Returns the MultiMesh data (such as instance transforms, colors, etc.).
See
`multimesh_set_buffer<class_RenderingServer_method_multimesh_set_buffer>`
for details on the returned data.

\*\*Note:\*\* If the buffer is in the engine's internal cache, it will
have to be fetched from GPU memory and possibly decompressed. This means
`multimesh_get_buffer<class_RenderingServer_method_multimesh_get_buffer>`
is potentially a slow operation and should be avoided whenever possible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AABB<class_AABB>` **multimesh\_get\_custom\_aabb**(multimesh:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_get_custom_aabb>`

Returns the custom AABB defined for this MultiMesh resource.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **multimesh\_get\_instance\_count**(multimesh:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_get_instance_count>`

Returns the number of instances allocated for this multimesh.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **multimesh\_get\_mesh**(multimesh: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_get_mesh>`

Returns the RID of the mesh that will be used in drawing this multimesh.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **multimesh\_get\_visible\_instances**(multimesh:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_get_visible_instances>`

Returns the number of visible instances for this multimesh.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **multimesh\_instance\_get\_color**(multimesh:
`RID<class_RID>`, index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_instance_get_color>`

Returns the color by which the specified instance will be modulated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>`
**multimesh\_instance\_get\_custom\_data**(multimesh: `RID<class_RID>`,
index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_instance_get_custom_data>`

Returns the custom data associated with the specified instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>`
**multimesh\_instance\_get\_transform**(multimesh: `RID<class_RID>`,
index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_instance_get_transform>`

Returns the `Transform3D<class_Transform3D>` of the specified instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>`
**multimesh\_instance\_get\_transform\_2d**(multimesh: `RID<class_RID>`,
index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_multimesh_instance_get_transform_2d>`

Returns the `Transform2D<class_Transform2D>` of the specified instance.
For use when the multimesh is set to use 2D transforms.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**multimesh\_instance\_reset\_physics\_interpolation**(multimesh:
`RID<class_RID>`, index: `int<class_int>`)
`🔗<class_RenderingServer_method_multimesh_instance_reset_physics_interpolation>`

Prevents physics interpolation for the specified instance during the
current physics tick.

This is useful when moving an instance to a new location, to give an
instantaneous change rather than interpolation from the previous
location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **multimesh\_instance\_set\_color**(multimesh:
`RID<class_RID>`, index: `int<class_int>`, color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_multimesh_instance_set_color>`

Sets the color by which this instance will be modulated. Equivalent to
`MultiMesh.set_instance_color<class_MultiMesh_method_set_instance_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**multimesh\_instance\_set\_custom\_data**(multimesh: `RID<class_RID>`,
index: `int<class_int>`, custom\_data: `Color<class_Color>`)
`🔗<class_RenderingServer_method_multimesh_instance_set_custom_data>`

Sets the custom data for this instance. Custom data is passed as a
`Color<class_Color>`, but is interpreted as a `vec4` in the shader.
Equivalent to
`MultiMesh.set_instance_custom_data<class_MultiMesh_method_set_instance_custom_data>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**multimesh\_instance\_set\_transform**(multimesh: `RID<class_RID>`,
index: `int<class_int>`, transform: `Transform3D<class_Transform3D>`)
`🔗<class_RenderingServer_method_multimesh_instance_set_transform>`

Sets the `Transform3D<class_Transform3D>` for this instance. Equivalent
to
`MultiMesh.set_instance_transform<class_MultiMesh_method_set_instance_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**multimesh\_instance\_set\_transform\_2d**(multimesh: `RID<class_RID>`,
index: `int<class_int>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_multimesh_instance_set_transform_2d>`

Sets the `Transform2D<class_Transform2D>` for this instance. For use
when multimesh is used in 2D. Equivalent to
`MultiMesh.set_instance_transform_2d<class_MultiMesh_method_set_instance_transform_2d>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **multimesh\_set\_buffer**(multimesh:
`RID<class_RID>`, buffer:
`PackedFloat32Array<class_PackedFloat32Array>`)
`🔗<class_RenderingServer_method_multimesh_set_buffer>`

Set the entire data to use for drawing the `multimesh` at once to
`buffer` (such as instance transforms and colors). `buffer`'s size must
match the number of instances multiplied by the per-instance data size
(which depends on the enabled MultiMesh fields). Otherwise, an error
message is printed and nothing is rendered. See also
`multimesh_get_buffer<class_RenderingServer_method_multimesh_get_buffer>`.

The per-instance data size and expected data order is:

    2D:
      - Position: 8 floats (8 floats for Transform2D)
      - Position + Vertex color: 12 floats (8 floats for Transform2D, 4 floats for Color)
      - Position + Custom data: 12 floats (8 floats for Transform2D, 4 floats of custom data)
      - Position + Vertex color + Custom data: 16 floats (8 floats for Transform2D, 4 floats for Color, 4 floats of custom data)
    3D:
      - Position: 12 floats (12 floats for Transform3D)
      - Position + Vertex color: 16 floats (12 floats for Transform3D, 4 floats for Color)
      - Position + Custom data: 16 floats (12 floats for Transform3D, 4 floats of custom data)
      - Position + Vertex color + Custom data: 20 floats (12 floats for Transform3D, 4 floats for Color, 4 floats of custom data)

Instance transforms are in row-major order. Specifically:

-   For `Transform2D<class_Transform2D>` the float-order is:
    `(x.x, y.x, padding_float, origin.x, x.y, y.y, padding_float, origin.y)`.
-   For `Transform3D<class_Transform3D>` the float-order is:
    `(basis.x.x, basis.y.x, basis.z.x, origin.x, basis.x.y, basis.y.y, basis.z.y, origin.y, basis.x.z, basis.y.z, basis.z.z, origin.z)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**multimesh\_set\_buffer\_interpolated**(multimesh: `RID<class_RID>`,
buffer: `PackedFloat32Array<class_PackedFloat32Array>`,
buffer\_previous: `PackedFloat32Array<class_PackedFloat32Array>`)
`🔗<class_RenderingServer_method_multimesh_set_buffer_interpolated>`

Alternative version of
`multimesh_set_buffer<class_RenderingServer_method_multimesh_set_buffer>`
for use with physics interpolation.

Takes both an array of current data and an array of data for the
previous physics tick.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **multimesh\_set\_custom\_aabb**(multimesh:
`RID<class_RID>`, aabb: `AABB<class_AABB>`)
`🔗<class_RenderingServer_method_multimesh_set_custom_aabb>`

Sets the custom AABB for this MultiMesh resource.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **multimesh\_set\_mesh**(multimesh:
`RID<class_RID>`, mesh: `RID<class_RID>`)
`🔗<class_RenderingServer_method_multimesh_set_mesh>`

Sets the mesh to be drawn by the multimesh. Equivalent to
`MultiMesh.mesh<class_MultiMesh_property_mesh>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**multimesh\_set\_physics\_interpolated**(multimesh: `RID<class_RID>`,
interpolated: `bool<class_bool>`)
`🔗<class_RenderingServer_method_multimesh_set_physics_interpolated>`

Turns on and off physics interpolation for this MultiMesh resource.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**multimesh\_set\_physics\_interpolation\_quality**(multimesh:
`RID<class_RID>`, quality:
`MultimeshPhysicsInterpolationQuality<enum_RenderingServer_MultimeshPhysicsInterpolationQuality>`)
`🔗<class_RenderingServer_method_multimesh_set_physics_interpolation_quality>`

Sets the physics interpolation quality for the
`MultiMesh<class_MultiMesh>`.

A value of
`MULTIMESH_INTERP_QUALITY_FAST<class_RenderingServer_constant_MULTIMESH_INTERP_QUALITY_FAST>`
gives fast but low quality interpolation, a value of
`MULTIMESH_INTERP_QUALITY_HIGH<class_RenderingServer_constant_MULTIMESH_INTERP_QUALITY_HIGH>`
gives slower but higher quality interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**multimesh\_set\_visible\_instances**(multimesh: `RID<class_RID>`,
visible: `int<class_int>`)
`🔗<class_RenderingServer_method_multimesh_set_visible_instances>`

Sets the number of instances visible at a given time. If -1, all
instances that have been allocated are drawn. Equivalent to
`MultiMesh.visible_instance_count<class_MultiMesh_property_visible_instance_count>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **occluder\_create**()
`🔗<class_RenderingServer_method_occluder_create>`

Creates an occluder instance and adds it to the RenderingServer. It can
be accessed with the RID that is returned. This RID will be used in all
`occluder_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is `Occluder3D<class_Occluder3D>`
(not to be confused with the
`OccluderInstance3D<class_OccluderInstance3D>` node).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **occluder\_set\_mesh**(occluder:
`RID<class_RID>`, vertices:
`PackedVector3Array<class_PackedVector3Array>`, indices:
`PackedInt32Array<class_PackedInt32Array>`)
`🔗<class_RenderingServer_method_occluder_set_mesh>`

Sets the mesh data for the given occluder RID, which controls the shape
of the occlusion culling that will be performed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **omni\_light\_create**()
`🔗<class_RenderingServer_method_omni_light_create>`

Creates a new omni light and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID can be used in most
`light_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach this omni light to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

\*\*Note:\*\* The equivalent node is `OmniLight3D<class_OmniLight3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **particles\_collision\_create**()
`🔗<class_RenderingServer_method_particles_collision_create>`

Creates a new 3D GPU particle collision or attractor and adds it to the
RenderingServer. It can be accessed with the RID that is returned. This
RID can be used in most `particles_collision_*` RenderingServer
functions.

\*\*Note:\*\* The equivalent nodes are
`GPUParticlesCollision3D<class_GPUParticlesCollision3D>` and
`GPUParticlesAttractor3D<class_GPUParticlesAttractor3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_height\_field\_update**(particles\_collision:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_collision_height_field_update>`

Requests an update for the 3D GPU particle collision heightfield. This
may be automatically called by the 3D GPU particle collision heightfield
depending on its
`GPUParticlesCollisionHeightField3D.update_mode<class_GPUParticlesCollisionHeightField3D_property_update_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_attractor\_attenuation**(particles\_collision:
`RID<class_RID>`, curve: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_collision_set_attractor_attenuation>`

Sets the attenuation `curve` for the 3D GPU particles attractor
specified by the `particles_collision` RID. Only used for attractors,
not colliders. Equivalent to
`GPUParticlesAttractor3D.attenuation<class_GPUParticlesAttractor3D_property_attenuation>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_attractor\_directionality**(particles\_collision:
`RID<class_RID>`, amount: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_collision_set_attractor_directionality>`

Sets the directionality `amount` for the 3D GPU particles attractor
specified by the `particles_collision` RID. Only used for attractors,
not colliders. Equivalent to
`GPUParticlesAttractor3D.directionality<class_GPUParticlesAttractor3D_property_directionality>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_attractor\_strength**(particles\_collision:
`RID<class_RID>`, strength: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_collision_set_attractor_strength>`

Sets the `strength` for the 3D GPU particles attractor specified by the
`particles_collision` RID. Only used for attractors, not colliders.
Equivalent to
`GPUParticlesAttractor3D.strength<class_GPUParticlesAttractor3D_property_strength>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_box\_extents**(particles\_collision:
`RID<class_RID>`, extents: `Vector3<class_Vector3>`)
`🔗<class_RenderingServer_method_particles_collision_set_box_extents>`

Sets the `extents` for the 3D GPU particles collision by the
`particles_collision` RID. Equivalent to
`GPUParticlesCollisionBox3D.size<class_GPUParticlesCollisionBox3D_property_size>`,
`GPUParticlesCollisionSDF3D.size<class_GPUParticlesCollisionSDF3D_property_size>`,
`GPUParticlesCollisionHeightField3D.size<class_GPUParticlesCollisionHeightField3D_property_size>`,
`GPUParticlesAttractorBox3D.size<class_GPUParticlesAttractorBox3D_property_size>`
or
`GPUParticlesAttractorVectorField3D.size<class_GPUParticlesAttractorVectorField3D_property_size>`
depending on the `particles_collision` type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_collision\_type**(particles\_collision:
`RID<class_RID>`, type:
`ParticlesCollisionType<enum_RenderingServer_ParticlesCollisionType>`)
`🔗<class_RenderingServer_method_particles_collision_set_collision_type>`

Sets the collision or attractor shape `type` for the 3D GPU particles
collision or attractor specified by the `particles_collision` RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_cull\_mask**(particles\_collision:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_RenderingServer_method_particles_collision_set_cull_mask>`

Sets the cull `mask` for the 3D GPU particles collision or attractor
specified by the `particles_collision` RID. Equivalent to
`GPUParticlesCollision3D.cull_mask<class_GPUParticlesCollision3D_property_cull_mask>`
or
`GPUParticlesAttractor3D.cull_mask<class_GPUParticlesAttractor3D_property_cull_mask>`
depending on the `particles_collision` type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_field\_texture**(particles\_collision:
`RID<class_RID>`, texture: `RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_collision_set_field_texture>`

Sets the signed distance field `texture` for the 3D GPU particles
collision specified by the `particles_collision` RID. Equivalent to
`GPUParticlesCollisionSDF3D.texture<class_GPUParticlesCollisionSDF3D_property_texture>`
or
`GPUParticlesAttractorVectorField3D.texture<class_GPUParticlesAttractorVectorField3D_property_texture>`
depending on the `particles_collision` type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_height\_field\_resolution**(particles\_collision:
`RID<class_RID>`, resolution:
`ParticlesCollisionHeightfieldResolution<enum_RenderingServer_ParticlesCollisionHeightfieldResolution>`)
`🔗<class_RenderingServer_method_particles_collision_set_height_field_resolution>`

Sets the heightmap `resolution` for the 3D GPU particles heightfield
collision specified by the `particles_collision` RID. Equivalent to
`GPUParticlesCollisionHeightField3D.resolution<class_GPUParticlesCollisionHeightField3D_property_resolution>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_collision\_set\_sphere\_radius**(particles\_collision:
`RID<class_RID>`, radius: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_collision_set_sphere_radius>`

Sets the `radius` for the 3D GPU particles sphere collision or attractor
specified by the `particles_collision` RID. Equivalent to
`GPUParticlesCollisionSphere3D.radius<class_GPUParticlesCollisionSphere3D_property_radius>`
or
`GPUParticlesAttractorSphere3D.radius<class_GPUParticlesAttractorSphere3D_property_radius>`
depending on the `particles_collision` type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **particles\_create**()
`🔗<class_RenderingServer_method_particles_create>`

Creates a GPU-based particle system and adds it to the RenderingServer.
It can be accessed with the RID that is returned. This RID will be used
in all `particles_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach these particles to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

\*\*Note:\*\* The equivalent nodes are
`GPUParticles2D<class_GPUParticles2D>` and
`GPUParticles3D<class_GPUParticles3D>`.

\*\*Note:\*\* All `particles_*` methods only apply to GPU-based
particles, not CPU-based particles.
`CPUParticles2D<class_CPUParticles2D>` and
`CPUParticles3D<class_CPUParticles3D>` do not have equivalent
RenderingServer functions available, as these use
`MultiMeshInstance2D<class_MultiMeshInstance2D>` and
`MultiMeshInstance3D<class_MultiMeshInstance3D>` under the hood (see
`multimesh_*` methods).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_emit**(particles:
`RID<class_RID>`, transform: `Transform3D<class_Transform3D>`, velocity:
`Vector3<class_Vector3>`, color: `Color<class_Color>`, custom:
`Color<class_Color>`, emit\_flags: `int<class_int>`)
`🔗<class_RenderingServer_method_particles_emit>`

Manually emits particles from the `particles` instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AABB<class_AABB>` **particles\_get\_current\_aabb**(particles:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_get_current_aabb>`

Calculates and returns the axis-aligned bounding box that contains all
the particles. Equivalent to
`GPUParticles3D.capture_aabb<class_GPUParticles3D_method_capture_aabb>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **particles\_get\_emitting**(particles:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_get_emitting>`

Returns `true` if particles are currently set to emitting.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **particles\_is\_inactive**(particles:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_is_inactive>`

Returns `true` if particles are not emitting and particles are set to
inactive.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_request\_process**(particles:
`RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_request_process>`

Add particle system to list of particle systems that need to be updated.
Update will take place on the next frame, or on the next call to
`instances_cull_aabb<class_RenderingServer_method_instances_cull_aabb>`,
`instances_cull_convex<class_RenderingServer_method_instances_cull_convex>`,
or
`instances_cull_ray<class_RenderingServer_method_instances_cull_ray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_restart**(particles:
`RID<class_RID>`) `🔗<class_RenderingServer_method_particles_restart>`

Reset the particles on the next update. Equivalent to
`GPUParticles3D.restart<class_GPUParticles3D_method_restart>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_amount**(particles:
`RID<class_RID>`, amount: `int<class_int>`)
`🔗<class_RenderingServer_method_particles_set_amount>`

Sets the number of particles to be drawn and allocates the memory for
them. Equivalent to
`GPUParticles3D.amount<class_GPUParticles3D_property_amount>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_amount\_ratio**(particles:
`RID<class_RID>`, ratio: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_amount_ratio>`

Sets the amount ratio for particles to be emitted. Equivalent to
`GPUParticles3D.amount_ratio<class_GPUParticles3D_property_amount_ratio>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_collision\_base\_size**(particles: `RID<class_RID>`,
size: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_collision_base_size>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_custom\_aabb**(particles:
`RID<class_RID>`, aabb: `AABB<class_AABB>`)
`🔗<class_RenderingServer_method_particles_set_custom_aabb>`

Sets a custom axis-aligned bounding box for the particle system.
Equivalent to
`GPUParticles3D.visibility_aabb<class_GPUParticles3D_property_visibility_aabb>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_draw\_order**(particles:
`RID<class_RID>`, order:
`ParticlesDrawOrder<enum_RenderingServer_ParticlesDrawOrder>`)
`🔗<class_RenderingServer_method_particles_set_draw_order>`

Sets the draw order of the particles to one of the named enums from
`ParticlesDrawOrder<enum_RenderingServer_ParticlesDrawOrder>`. See
`ParticlesDrawOrder<enum_RenderingServer_ParticlesDrawOrder>` for
options. Equivalent to
`GPUParticles3D.draw_order<class_GPUParticles3D_property_draw_order>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_draw\_pass\_mesh**(particles: `RID<class_RID>`, pass:
`int<class_int>`, mesh: `RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_set_draw_pass_mesh>`

Sets the mesh to be used for the specified draw pass. Equivalent to
`GPUParticles3D.draw_pass_1<class_GPUParticles3D_property_draw_pass_1>`,
`GPUParticles3D.draw_pass_2<class_GPUParticles3D_property_draw_pass_2>`,
`GPUParticles3D.draw_pass_3<class_GPUParticles3D_property_draw_pass_3>`,
and
`GPUParticles3D.draw_pass_4<class_GPUParticles3D_property_draw_pass_4>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_draw\_passes**(particles:
`RID<class_RID>`, count: `int<class_int>`)
`🔗<class_RenderingServer_method_particles_set_draw_passes>`

Sets the number of draw passes to use. Equivalent to
`GPUParticles3D.draw_passes<class_GPUParticles3D_property_draw_passes>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_emission\_transform**(particles: `RID<class_RID>`,
transform: `Transform3D<class_Transform3D>`)
`🔗<class_RenderingServer_method_particles_set_emission_transform>`

Sets the `Transform3D<class_Transform3D>` that will be used by the
particles when they first emit.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_emitter\_velocity**(particles: `RID<class_RID>`,
velocity: `Vector3<class_Vector3>`)
`🔗<class_RenderingServer_method_particles_set_emitter_velocity>`

Sets the velocity of a particle node, that will be used by
`ParticleProcessMaterial.inherit_velocity_ratio<class_ParticleProcessMaterial_property_inherit_velocity_ratio>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_emitting**(particles:
`RID<class_RID>`, emitting: `bool<class_bool>`)
`🔗<class_RenderingServer_method_particles_set_emitting>`

If `true`, particles will emit over time. Setting to false does not
reset the particles, but only stops their emission. Equivalent to
`GPUParticles3D.emitting<class_GPUParticles3D_property_emitting>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_explosiveness\_ratio**(particles: `RID<class_RID>`,
ratio: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_explosiveness_ratio>`

Sets the explosiveness ratio. Equivalent to
`GPUParticles3D.explosiveness<class_GPUParticles3D_property_explosiveness>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_fixed\_fps**(particles:
`RID<class_RID>`, fps: `int<class_int>`)
`🔗<class_RenderingServer_method_particles_set_fixed_fps>`

Sets the frame rate that the particle system rendering will be fixed to.
Equivalent to
`GPUParticles3D.fixed_fps<class_GPUParticles3D_property_fixed_fps>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_fractional\_delta**(particles: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_particles_set_fractional_delta>`

If `true`, uses fractional delta which smooths the movement of the
particles. Equivalent to
`GPUParticles3D.fract_delta<class_GPUParticles3D_property_fract_delta>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_interp\_to\_end**(particles:
`RID<class_RID>`, factor: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_interp_to_end>`

Sets the value that informs a
`ParticleProcessMaterial<class_ParticleProcessMaterial>` to rush all
particles towards the end of their lifetime.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_interpolate**(particles:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_particles_set_interpolate>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_lifetime**(particles:
`RID<class_RID>`, lifetime: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_lifetime>`

Sets the lifetime of each particle in the system. Equivalent to
`GPUParticles3D.lifetime<class_GPUParticles3D_property_lifetime>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_mode**(particles:
`RID<class_RID>`, mode:
`ParticlesMode<enum_RenderingServer_ParticlesMode>`)
`🔗<class_RenderingServer_method_particles_set_mode>`

Sets whether the GPU particles specified by the `particles` RID should
be rendered in 2D or 3D according to `mode`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_one\_shot**(particles:
`RID<class_RID>`, one\_shot: `bool<class_bool>`)
`🔗<class_RenderingServer_method_particles_set_one_shot>`

If `true`, particles will emit once and then stop. Equivalent to
`GPUParticles3D.one_shot<class_GPUParticles3D_property_one_shot>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_pre\_process\_time**(particles: `RID<class_RID>`,
time: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_pre_process_time>`

Sets the preprocess time for the particles' animation. This lets you
delay starting an animation until after the particles have begun
emitting. Equivalent to
`GPUParticles3D.preprocess<class_GPUParticles3D_property_preprocess>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_process\_material**(particles: `RID<class_RID>`,
material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_set_process_material>`

Sets the material for processing the particles.

\*\*Note:\*\* This is not the material used to draw the materials.
Equivalent to
`GPUParticles3D.process_material<class_GPUParticles3D_property_process_material>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_randomness\_ratio**(particles: `RID<class_RID>`,
ratio: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_randomness_ratio>`

Sets the emission randomness ratio. This randomizes the emission of
particles within their phase. Equivalent to
`GPUParticles3D.randomness<class_GPUParticles3D_property_randomness>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_speed\_scale**(particles:
`RID<class_RID>`, scale: `float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_speed_scale>`

Sets the speed scale of the particle system. Equivalent to
`GPUParticles3D.speed_scale<class_GPUParticles3D_property_speed_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_subemitter**(particles:
`RID<class_RID>`, subemitter\_particles: `RID<class_RID>`)
`🔗<class_RenderingServer_method_particles_set_subemitter>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_trail\_bind\_poses**(particles: `RID<class_RID>`,
bind\_poses: `Array<class_Array>`\[`Transform3D<class_Transform3D>`\])
`🔗<class_RenderingServer_method_particles_set_trail_bind_poses>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **particles\_set\_trails**(particles:
`RID<class_RID>`, enable: `bool<class_bool>`, length\_sec:
`float<class_float>`)
`🔗<class_RenderingServer_method_particles_set_trails>`

If `enable` is `true`, enables trails for the `particles` with the
specified `length_sec` in seconds. Equivalent to
`GPUParticles3D.trail_enabled<class_GPUParticles3D_property_trail_enabled>`
and
`GPUParticles3D.trail_lifetime<class_GPUParticles3D_property_trail_lifetime>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_transform\_align**(particles: `RID<class_RID>`, align:
`ParticlesTransformAlign<enum_RenderingServer_ParticlesTransformAlign>`)
`🔗<class_RenderingServer_method_particles_set_transform_align>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**particles\_set\_use\_local\_coordinates**(particles: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_particles_set_use_local_coordinates>`

If `true`, particles use local coordinates. If `false` they use global
coordinates. Equivalent to
`GPUParticles3D.local_coords<class_GPUParticles3D_property_local_coords>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**positional\_soft\_shadow\_filter\_set\_quality**(quality:
`ShadowQuality<enum_RenderingServer_ShadowQuality>`)
`🔗<class_RenderingServer_method_positional_soft_shadow_filter_set_quality>`

Sets the filter quality for omni and spot light shadows in 3D. See also
`ProjectSettings.rendering/lights_and_shadows/positional_shadow/soft_shadow_filter_quality<class_ProjectSettings_property_rendering/lights_and_shadows/positional_shadow/soft_shadow_filter_quality>`.
This parameter is global and cannot be set on a per-viewport basis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **reflection\_probe\_create**()
`🔗<class_RenderingServer_method_reflection_probe_create>`

Creates a reflection probe and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`reflection_probe_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach this reflection probe to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

\*\*Note:\*\* The equivalent node is
`ReflectionProbe<class_ReflectionProbe>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_ambient\_color**(probe: `RID<class_RID>`,
color: `Color<class_Color>`)
`🔗<class_RenderingServer_method_reflection_probe_set_ambient_color>`

Sets the reflection probe's custom ambient light color. Equivalent to
`ReflectionProbe.ambient_color<class_ReflectionProbe_property_ambient_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_ambient\_energy**(probe: `RID<class_RID>`,
energy: `float<class_float>`)
`🔗<class_RenderingServer_method_reflection_probe_set_ambient_energy>`

Sets the reflection probe's custom ambient light energy. Equivalent to
`ReflectionProbe.ambient_color_energy<class_ReflectionProbe_property_ambient_color_energy>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_ambient\_mode**(probe: `RID<class_RID>`, mode:
`ReflectionProbeAmbientMode<enum_RenderingServer_ReflectionProbeAmbientMode>`)
`🔗<class_RenderingServer_method_reflection_probe_set_ambient_mode>`

Sets the reflection probe's ambient light mode. Equivalent to
`ReflectionProbe.ambient_mode<class_ReflectionProbe_property_ambient_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_as\_interior**(probe: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_reflection_probe_set_as_interior>`

If `true`, reflections will ignore sky contribution. Equivalent to
`ReflectionProbe.interior<class_ReflectionProbe_property_interior>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reflection\_probe\_set\_cull\_mask**(probe:
`RID<class_RID>`, layers: `int<class_int>`)
`🔗<class_RenderingServer_method_reflection_probe_set_cull_mask>`

Sets the render cull mask for this reflection probe. Only instances with
a matching layer will be reflected by this probe. Equivalent to
`ReflectionProbe.cull_mask<class_ReflectionProbe_property_cull_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_enable\_box\_projection**(probe:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_reflection_probe_set_enable_box_projection>`

If `true`, uses box projection. This can make reflections look more
correct in certain situations. Equivalent to
`ReflectionProbe.box_projection<class_ReflectionProbe_property_box_projection>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_enable\_shadows**(probe: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_reflection_probe_set_enable_shadows>`

If `true`, computes shadows in the reflection probe. This makes the
reflection much slower to compute. Equivalent to
`ReflectionProbe.enable_shadows<class_ReflectionProbe_property_enable_shadows>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reflection\_probe\_set\_intensity**(probe:
`RID<class_RID>`, intensity: `float<class_float>`)
`🔗<class_RenderingServer_method_reflection_probe_set_intensity>`

Sets the intensity of the reflection probe. Intensity modulates the
strength of the reflection. Equivalent to
`ReflectionProbe.intensity<class_ReflectionProbe_property_intensity>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_max\_distance**(probe: `RID<class_RID>`,
distance: `float<class_float>`)
`🔗<class_RenderingServer_method_reflection_probe_set_max_distance>`

Sets the max distance away from the probe an object can be before it is
culled. Equivalent to
`ReflectionProbe.max_distance<class_ReflectionProbe_property_max_distance>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_mesh\_lod\_threshold**(probe:
`RID<class_RID>`, pixels: `float<class_float>`)
`🔗<class_RenderingServer_method_reflection_probe_set_mesh_lod_threshold>`

Sets the mesh level of detail to use in the reflection probe rendering.
Higher values will use less detailed versions of meshes that have LOD
variations generated, which can improve performance. Equivalent to
`ReflectionProbe.mesh_lod_threshold<class_ReflectionProbe_property_mesh_lod_threshold>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_origin\_offset**(probe: `RID<class_RID>`,
offset: `Vector3<class_Vector3>`)
`🔗<class_RenderingServer_method_reflection_probe_set_origin_offset>`

Sets the origin offset to be used when this reflection probe is in box
project mode. Equivalent to
`ReflectionProbe.origin_offset<class_ReflectionProbe_property_origin_offset>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_reflection\_mask**(probe: `RID<class_RID>`,
layers: `int<class_int>`)
`🔗<class_RenderingServer_method_reflection_probe_set_reflection_mask>`

Sets the render reflection mask for this reflection probe. Only
instances with a matching layer will have reflections applied from this
probe. Equivalent to
`ReflectionProbe.reflection_mask<class_ReflectionProbe_property_reflection_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reflection\_probe\_set\_resolution**(probe:
`RID<class_RID>`, resolution: `int<class_int>`)
`🔗<class_RenderingServer_method_reflection_probe_set_resolution>`

Sets the resolution to use when rendering the specified reflection
probe. The `resolution` is specified for each cubemap face: for
instance, specifying `512` will allocate 6 faces of 512×512 each (plus
mipmaps for roughness levels).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reflection\_probe\_set\_size**(probe:
`RID<class_RID>`, size: `Vector3<class_Vector3>`)
`🔗<class_RenderingServer_method_reflection_probe_set_size>`

Sets the size of the area that the reflection probe will capture.
Equivalent to
`ReflectionProbe.size<class_ReflectionProbe_property_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**reflection\_probe\_set\_update\_mode**(probe: `RID<class_RID>`, mode:
`ReflectionProbeUpdateMode<enum_RenderingServer_ReflectionProbeUpdateMode>`)
`🔗<class_RenderingServer_method_reflection_probe_set_update_mode>`

Sets how often the reflection probe updates. Can either be once or every
frame. See
`ReflectionProbeUpdateMode<enum_RenderingServer_ReflectionProbeUpdateMode>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **request\_frame\_drawn\_callback**(callable:
`Callable<class_Callable>`)
`🔗<class_RenderingServer_method_request_frame_drawn_callback>`

Schedules a callback to the given callable after a frame has been drawn.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **scenario\_create**()
`🔗<class_RenderingServer_method_scenario_create>`

Creates a scenario and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`scenario_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

The scenario is the 3D world that all the visual instances exist in.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**scenario\_set\_camera\_attributes**(scenario: `RID<class_RID>`,
effects: `RID<class_RID>`)
`🔗<class_RenderingServer_method_scenario_set_camera_attributes>`

Sets the camera attributes (`effects`) that will be used with this
scenario. See also `CameraAttributes<class_CameraAttributes>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **scenario\_set\_compositor**(scenario:
`RID<class_RID>`, compositor: `RID<class_RID>`)
`🔗<class_RenderingServer_method_scenario_set_compositor>`

Sets the compositor (`compositor`) that will be used with this scenario.
See also `Compositor<class_Compositor>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **scenario\_set\_environment**(scenario:
`RID<class_RID>`, environment: `RID<class_RID>`)
`🔗<class_RenderingServer_method_scenario_set_environment>`

Sets the environment that will be used with this scenario. See also
`Environment<class_Environment>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**scenario\_set\_fallback\_environment**(scenario: `RID<class_RID>`,
environment: `RID<class_RID>`)
`🔗<class_RenderingServer_method_scenario_set_fallback_environment>`

Sets the fallback environment to be used by this scenario. The fallback
environment is used if no environment is set. Internally, this is used
by the editor to provide a default environment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**screen\_space\_roughness\_limiter\_set\_active**(enable:
`bool<class_bool>`, amount: `float<class_float>`, limit:
`float<class_float>`)
`🔗<class_RenderingServer_method_screen_space_roughness_limiter_set_active>`

Sets the screen-space roughness limiter parameters, such as whether it
should be enabled and its thresholds. Equivalent to
`ProjectSettings.rendering/anti_aliasing/screen_space_roughness_limiter/enabled<class_ProjectSettings_property_rendering/anti_aliasing/screen_space_roughness_limiter/enabled>`,
`ProjectSettings.rendering/anti_aliasing/screen_space_roughness_limiter/amount<class_ProjectSettings_property_rendering/anti_aliasing/screen_space_roughness_limiter/amount>`
and
`ProjectSettings.rendering/anti_aliasing/screen_space_roughness_limiter/limit<class_ProjectSettings_property_rendering/anti_aliasing/screen_space_roughness_limiter/limit>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_boot\_image**(image:
`Image<class_Image>`, color: `Color<class_Color>`, scale:
`bool<class_bool>`, use\_filter: `bool<class_bool>` = true)
`🔗<class_RenderingServer_method_set_boot_image>`

Sets a boot image. The color defines the background color. If `scale` is
`true`, the image will be scaled to fit the screen size. If `use_filter`
is `true`, the image will be scaled with linear interpolation. If
`use_filter` is `false`, the image will be scaled with nearest-neighbor
interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_debug\_generate\_wireframes**(generate:
`bool<class_bool>`)
`🔗<class_RenderingServer_method_set_debug_generate_wireframes>`

This method is currently unimplemented and does nothing if called with
`generate` set to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_default\_clear\_color**(color:
`Color<class_Color>`)
`🔗<class_RenderingServer_method_set_default_clear_color>`

Sets the default clear color which is used when a specific clear color
has not been selected. See also
`get_default_clear_color<class_RenderingServer_method_get_default_clear_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **shader\_create**()
`🔗<class_RenderingServer_method_shader_create>`

Creates an empty shader and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`shader_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is `Shader<class_Shader>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **shader\_get\_code**(shader: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_shader_get_code>`

Returns a shader's source code as a string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **shader\_get\_default\_texture\_parameter**(shader:
`RID<class_RID>`, name: `StringName<class_StringName>`, index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_shader_get_default_texture_parameter>`

Returns a default texture from a shader searched by name.

\*\*Note:\*\* If the sampler array is used use `index` to access the
specified texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **shader\_get\_parameter\_default**(shader:
`RID<class_RID>`, name: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_shader_get_parameter_default>`

Returns the default value for the specified shader uniform. This is
usually the value written in the shader source code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **shader\_set\_code**(shader:
`RID<class_RID>`, code: `String<class_String>`)
`🔗<class_RenderingServer_method_shader_set_code>`

Sets the shader's source code (which triggers recompilation after being
changed).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**shader\_set\_default\_texture\_parameter**(shader: `RID<class_RID>`,
name: `StringName<class_StringName>`, texture: `RID<class_RID>`, index:
`int<class_int>` = 0)
`🔗<class_RenderingServer_method_shader_set_default_texture_parameter>`

Sets a shader's default texture. Overwrites the texture given by name.

\*\*Note:\*\* If the sampler array is used use `index` to access the
specified texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **shader\_set\_path\_hint**(shader:
`RID<class_RID>`, path: `String<class_String>`)
`🔗<class_RenderingServer_method_shader_set_path_hint>`

Sets the path hint for the specified shader. This should generally match
the `Shader<class_Shader>` resource's
`Resource.resource_path<class_Resource_property_resource_path>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **skeleton\_allocate\_data**(skeleton:
`RID<class_RID>`, bones: `int<class_int>`, is\_2d\_skeleton:
`bool<class_bool>` = false)
`🔗<class_RenderingServer_method_skeleton_allocate_data>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>`
**skeleton\_bone\_get\_transform**(skeleton: `RID<class_RID>`, bone:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_skeleton_bone_get_transform>`

Returns the `Transform3D<class_Transform3D>` set for a specific bone of
this skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>`
**skeleton\_bone\_get\_transform\_2d**(skeleton: `RID<class_RID>`, bone:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_skeleton_bone_get_transform_2d>`

Returns the `Transform2D<class_Transform2D>` set for a specific bone of
this skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **skeleton\_bone\_set\_transform**(skeleton:
`RID<class_RID>`, bone: `int<class_int>`, transform:
`Transform3D<class_Transform3D>`)
`🔗<class_RenderingServer_method_skeleton_bone_set_transform>`

Sets the `Transform3D<class_Transform3D>` for a specific bone of this
skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**skeleton\_bone\_set\_transform\_2d**(skeleton: `RID<class_RID>`, bone:
`int<class_int>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_skeleton_bone_set_transform_2d>`

Sets the `Transform2D<class_Transform2D>` for a specific bone of this
skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **skeleton\_create**()
`🔗<class_RenderingServer_method_skeleton_create>`

Creates a skeleton and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`skeleton_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **skeleton\_get\_bone\_count**(skeleton:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_skeleton_get_bone_count>`

Returns the number of bones allocated for this skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**skeleton\_set\_base\_transform\_2d**(skeleton: `RID<class_RID>`,
base\_transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_skeleton_set_base_transform_2d>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **sky\_bake\_panorama**(sky: `RID<class_RID>`,
energy: `float<class_float>`, bake\_irradiance: `bool<class_bool>`,
size: `Vector2i<class_Vector2i>`)
`🔗<class_RenderingServer_method_sky_bake_panorama>`

Generates and returns an `Image<class_Image>` containing the radiance
map for the specified `sky` RID. This supports built-in sky material and
custom sky shaders. If `bake_irradiance` is `true`, the irradiance map
is saved instead of the radiance map. The radiance map is used to render
reflected light, while the irradiance map is used to render ambient
light. See also
`environment_bake_panorama<class_RenderingServer_method_environment_bake_panorama>`.

\*\*Note:\*\* The image is saved in linear color space without any
tonemapping performed, which means it will look too dark if viewed
directly in an image editor. `energy` values above `1.0` can be used to
brighten the resulting image.

\*\*Note:\*\* `size` should be a 2:1 aspect ratio for the generated
panorama to have square pixels. For radiance maps, there is no point in
using a height greater than
`Sky.radiance_size<class_Sky_property_radiance_size>`, as it won't
increase detail. Irradiance maps only contain low-frequency data, so
there is usually no point in going past a size of 128×64 pixels when
saving an irradiance map.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **sky\_create**()
`🔗<class_RenderingServer_method_sky_create>`

Creates an empty sky and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`sky_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **sky\_set\_material**(sky: `RID<class_RID>`,
material: `RID<class_RID>`)
`🔗<class_RenderingServer_method_sky_set_material>`

Sets the material that the sky uses to render the background, ambient
and reflection maps.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **sky\_set\_mode**(sky: `RID<class_RID>`,
mode: `SkyMode<enum_RenderingServer_SkyMode>`)
`🔗<class_RenderingServer_method_sky_set_mode>`

Sets the process `mode` of the sky specified by the `sky` RID.
Equivalent to `Sky.process_mode<class_Sky_property_process_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **sky\_set\_radiance\_size**(sky:
`RID<class_RID>`, radiance\_size: `int<class_int>`)
`🔗<class_RenderingServer_method_sky_set_radiance_size>`

Sets the `radiance_size` of the sky specified by the `sky` RID (in
pixels). Equivalent to
`Sky.radiance_size<class_Sky_property_radiance_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **spot\_light\_create**()
`🔗<class_RenderingServer_method_spot_light_create>`

Creates a spot light and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID can be used in most
`light_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach this spot light to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**sub\_surface\_scattering\_set\_quality**(quality:
`SubSurfaceScatteringQuality<enum_RenderingServer_SubSurfaceScatteringQuality>`)
`🔗<class_RenderingServer_method_sub_surface_scattering_set_quality>`

Sets
`ProjectSettings.rendering/environment/subsurface_scattering/subsurface_scattering_quality<class_ProjectSettings_property_rendering/environment/subsurface_scattering/subsurface_scattering_quality>`
to use when rendering materials that have subsurface scattering enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**sub\_surface\_scattering\_set\_scale**(scale: `float<class_float>`,
depth\_scale: `float<class_float>`)
`🔗<class_RenderingServer_method_sub_surface_scattering_set_scale>`

Sets the
`ProjectSettings.rendering/environment/subsurface_scattering/subsurface_scattering_scale<class_ProjectSettings_property_rendering/environment/subsurface_scattering/subsurface_scattering_scale>`
and
`ProjectSettings.rendering/environment/subsurface_scattering/subsurface_scattering_depth_scale<class_ProjectSettings_property_rendering/environment/subsurface_scattering/subsurface_scattering_depth_scale>`
to use when rendering materials that have subsurface scattering enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_2d\_create**(image: `Image<class_Image>`)
`🔗<class_RenderingServer_method_texture_2d_create>`

Creates a 2-dimensional texture and adds it to the RenderingServer. It
can be accessed with the RID that is returned. This RID will be used in
all `texture_2d_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is `Texture2D<class_Texture2D>`.

\*\*Note:\*\* Not to be confused with
`RenderingDevice.texture_create<class_RenderingDevice_method_texture_create>`,
which creates the graphics API's own texture type as opposed to the
Godot-specific `Texture2D<class_Texture2D>` resource.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **texture\_2d\_get**(texture: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_texture_2d_get>`

Returns an `Image<class_Image>` instance from the given `texture`
`RID<class_RID>`.

Example of getting the test texture from
`get_test_texture<class_RenderingServer_method_get_test_texture>` and
applying it to a `Sprite2D<class_Sprite2D>` node:

    var texture_rid = RenderingServer.get_test_texture()
    var texture = ImageTexture.create_from_image(RenderingServer.texture_2d_get(texture_rid))
    $Sprite2D.texture = texture

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **texture\_2d\_layer\_get**(texture:
`RID<class_RID>`, layer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_texture_2d_layer_get>`

Returns an `Image<class_Image>` instance from the given `texture`
`RID<class_RID>` and `layer`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_2d\_layered\_create**(layers:
`Array<class_Array>`\[`Image<class_Image>`\], layered\_type:
`TextureLayeredType<enum_RenderingServer_TextureLayeredType>`)
`🔗<class_RenderingServer_method_texture_2d_layered_create>`

Creates a 2-dimensional layered texture and adds it to the
RenderingServer. It can be accessed with the RID that is returned. This
RID will be used in all `texture_2d_layered_*` RenderingServer
functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is
`TextureLayered<class_TextureLayered>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>`
**texture\_2d\_layered\_placeholder\_create**(layered\_type:
`TextureLayeredType<enum_RenderingServer_TextureLayeredType>`)
`🔗<class_RenderingServer_method_texture_2d_layered_placeholder_create>`

Creates a placeholder for a 2-dimensional layered texture and adds it to
the RenderingServer. It can be accessed with the RID that is returned.
This RID will be used in all `texture_2d_layered_*` RenderingServer
functions, although it does nothing when used. See also
`texture_2d_placeholder_create<class_RenderingServer_method_texture_2d_placeholder_create>`.

\*\*Note:\*\* The equivalent resource is
`PlaceholderTextureLayered<class_PlaceholderTextureLayered>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_2d\_placeholder\_create**()
`🔗<class_RenderingServer_method_texture_2d_placeholder_create>`

Creates a placeholder for a 2-dimensional layered texture and adds it to
the RenderingServer. It can be accessed with the RID that is returned.
This RID will be used in all `texture_2d_layered_*` RenderingServer
functions, although it does nothing when used. See also
`texture_2d_layered_placeholder_create<class_RenderingServer_method_texture_2d_layered_placeholder_create>`.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is
`PlaceholderTexture2D<class_PlaceholderTexture2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **texture\_2d\_update**(texture:
`RID<class_RID>`, image: `Image<class_Image>`, layer: `int<class_int>`)
`🔗<class_RenderingServer_method_texture_2d_update>`

Updates the texture specified by the `texture` `RID<class_RID>` with the
data in `image`. A `layer` must also be specified, which should be `0`
when updating a single-layer texture (`Texture2D<class_Texture2D>`).

\*\*Note:\*\* The `image` must have the same width, height and format as
the current `texture` data. Otherwise, an error will be printed and the
original texture won't be modified. If you need to use different width,
height or format, use
`texture_replace<class_RenderingServer_method_texture_replace>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_3d\_create**(format:
`Format<enum_Image_Format>`, width: `int<class_int>`, height:
`int<class_int>`, depth: `int<class_int>`, mipmaps: `bool<class_bool>`,
data: `Array<class_Array>`\[`Image<class_Image>`\])
`🔗<class_RenderingServer_method_texture_3d_create>`

**Note:** The equivalent resource is `Texture3D<class_Texture3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Image<class_Image>`\]
**texture\_3d\_get**(texture: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_texture_3d_get>`

Returns 3D texture data as an array of `Image<class_Image>`s for the
specified texture `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_3d\_placeholder\_create**()
`🔗<class_RenderingServer_method_texture_3d_placeholder_create>`

Creates a placeholder for a 3-dimensional texture and adds it to the
RenderingServer. It can be accessed with the RID that is returned. This
RID will be used in all `texture_3d_*` RenderingServer functions,
although it does nothing when used.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent resource is
`PlaceholderTexture3D<class_PlaceholderTexture3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **texture\_3d\_update**(texture:
`RID<class_RID>`, data: `Array<class_Array>`\[`Image<class_Image>`\])
`🔗<class_RenderingServer_method_texture_3d_update>`

Updates the texture specified by the `texture` `RID<class_RID>`'s data
with the data in `data`. All the texture's layers must be replaced at
once.

\*\*Note:\*\* The `texture` must have the same width, height, depth and
format as the current texture data. Otherwise, an error will be printed
and the original texture won't be modified. If you need to use different
width, height, depth or format, use
`texture_replace<class_RenderingServer_method_texture_replace>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_create\_from\_native\_handle**(type:
`TextureType<enum_RenderingServer_TextureType>`, format:
`Format<enum_Image_Format>`, native\_handle: `int<class_int>`, width:
`int<class_int>`, height: `int<class_int>`, depth: `int<class_int>`,
layers: `int<class_int>` = 1, layered\_type:
`TextureLayeredType<enum_RenderingServer_TextureLayeredType>` = 0)
`🔗<class_RenderingServer_method_texture_create_from_native_handle>`

Creates a texture based on a native handle that was created outside of
Godot's renderer.

\*\*Note:\*\* If using the rendering device renderer, using
`RenderingDevice.texture_create_from_extension<class_RenderingDevice_method_texture_create_from_extension>`
rather than this method is recommended. It will give you much more
control over the texture's format and usage.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Format<enum_Image_Format>` **texture\_get\_format**(texture:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_texture_get_format>`

Returns the format for the texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **texture\_get\_native\_handle**(texture:
`RID<class_RID>`, srgb: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_texture_get_native_handle>`

Returns the internal graphics handle for this texture object. For use
when communicating with third-party APIs mostly with GDExtension.

\*\*Note:\*\* This function returns a `uint64_t` which internally maps
to a `GLuint` (OpenGL) or `VkImage` (Vulkan).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **texture\_get\_path**(texture: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_texture_get_path>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_get\_rd\_texture**(texture:
`RID<class_RID>`, srgb: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_texture_get_rd_texture>`

Returns a texture `RID<class_RID>` that can be used with
`RenderingDevice<class_RenderingDevice>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_proxy\_create**(base: `RID<class_RID>`)
`🔗<class_RenderingServer_method_texture_proxy_create>`

**Deprecated:** ProxyTexture was removed in Godot 4.

This method does nothing and always returns an invalid `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **texture\_proxy\_update**(texture:
`RID<class_RID>`, proxy\_to: `RID<class_RID>`)
`🔗<class_RenderingServer_method_texture_proxy_update>`

**Deprecated:** ProxyTexture was removed in Godot 4.

This method does nothing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_rd\_create**(rd\_texture: `RID<class_RID>`,
layer\_type:
`TextureLayeredType<enum_RenderingServer_TextureLayeredType>` = 0)
`🔗<class_RenderingServer_method_texture_rd_create>`

Creates a new texture object based on a texture created directly on the
`RenderingDevice<class_RenderingDevice>`. If the texture contains
layers, `layer_type` is used to define the layer type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **texture\_replace**(texture:
`RID<class_RID>`, by\_texture: `RID<class_RID>`)
`🔗<class_RenderingServer_method_texture_replace>`

Replaces `texture`'s texture data by the texture specified by the
`by_texture` RID, without changing `texture`'s RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**texture\_set\_force\_redraw\_if\_visible**(texture: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_texture_set_force_redraw_if_visible>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **texture\_set\_path**(texture:
`RID<class_RID>`, path: `String<class_String>`)
`🔗<class_RenderingServer_method_texture_set_path>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **texture\_set\_size\_override**(texture:
`RID<class_RID>`, width: `int<class_int>`, height: `int<class_int>`)
`🔗<class_RenderingServer_method_texture_set_size_override>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_attach\_camera**(viewport:
`RID<class_RID>`, camera: `RID<class_RID>`)
`🔗<class_RenderingServer_method_viewport_attach_camera>`

Sets a viewport's camera.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_attach\_canvas**(viewport:
`RID<class_RID>`, canvas: `RID<class_RID>`)
`🔗<class_RenderingServer_method_viewport_attach_canvas>`

Sets a viewport's canvas.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_attach\_to\_screen**(viewport:
`RID<class_RID>`, rect: `Rect2<class_Rect2>` = Rect2(0, 0, 0, 0),
screen: `int<class_int>` = 0)
`🔗<class_RenderingServer_method_viewport_attach_to_screen>`

Copies the viewport to a region of the screen specified by `rect`. If
`viewport_set_render_direct_to_screen<class_RenderingServer_method_viewport_set_render_direct_to_screen>`
is `true`, then the viewport does not use a framebuffer and the contents
of the viewport are rendered directly to screen. However, note that the
root viewport is drawn last, therefore it will draw over the screen.
Accordingly, you must set the root viewport to an area that does not
cover the area that you have attached this viewport to.

For example, you can set the root viewport to not render at all with the
following code:

FIXME: The method seems to be non-existent.

gdscript

func \_ready():  
get\_viewport().set\_attach\_to\_screen\_rect(Rect2())
$Viewport.set\_attach\_to\_screen\_rect(Rect2(0, 0, 600, 600))

Using this can result in significant optimization, especially on
lower-end devices. However, it comes at the cost of having to manage
your viewports manually. For further optimization, see
`viewport_set_render_direct_to_screen<class_RenderingServer_method_viewport_set_render_direct_to_screen>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **viewport\_create**()
`🔗<class_RenderingServer_method_viewport_create>`

Creates an empty viewport and adds it to the RenderingServer. It can be
accessed with the RID that is returned. This RID will be used in all
`viewport_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent node is `Viewport<class_Viewport>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**viewport\_get\_measured\_render\_time\_cpu**(viewport:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_viewport_get_measured_render_time_cpu>`

Returns the CPU time taken to render the last frame in milliseconds.
This *only* includes time spent in rendering-related operations;
scripts' `_process` functions and other engine subsystems are not
included in this readout. To get a complete readout of CPU time spent to
render the scene, sum the render times of all viewports that are drawn
every frame plus
`get_frame_setup_time_cpu<class_RenderingServer_method_get_frame_setup_time_cpu>`.
Unlike
`Engine.get_frames_per_second<class_Engine_method_get_frames_per_second>`,
this method will accurately reflect CPU utilization even if framerate is
capped via V-Sync or `Engine.max_fps<class_Engine_property_max_fps>`.
See also
`viewport_get_measured_render_time_gpu<class_RenderingServer_method_viewport_get_measured_render_time_gpu>`.

\*\*Note:\*\* Requires measurements to be enabled on the specified
`viewport` using
`viewport_set_measure_render_time<class_RenderingServer_method_viewport_set_measure_render_time>`.
Otherwise, this method returns `0.0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**viewport\_get\_measured\_render\_time\_gpu**(viewport:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_viewport_get_measured_render_time_gpu>`

Returns the GPU time taken to render the last frame in milliseconds. To
get a complete readout of GPU time spent to render the scene, sum the
render times of all viewports that are drawn every frame. Unlike
`Engine.get_frames_per_second<class_Engine_method_get_frames_per_second>`,
this method accurately reflects GPU utilization even if framerate is
capped via V-Sync or `Engine.max_fps<class_Engine_property_max_fps>`.
See also
`viewport_get_measured_render_time_cpu<class_RenderingServer_method_viewport_get_measured_render_time_cpu>`.

\*\*Note:\*\* Requires measurements to be enabled on the specified
`viewport` using
`viewport_set_measure_render_time<class_RenderingServer_method_viewport_set_measure_render_time>`.
Otherwise, this method returns `0.0`.

\*\*Note:\*\* When GPU utilization is low enough during a certain period
of time, GPUs will decrease their power state (which in turn decreases
core and memory clock speeds). This can cause the reported GPU time to
increase if GPU utilization is kept low enough by a framerate cap
(compared to what it would be at the GPU's highest power state). Keep
this in mind when benchmarking using
`viewport_get_measured_render_time_gpu<class_RenderingServer_method_viewport_get_measured_render_time_gpu>`.
This behavior can be overridden in the graphics driver settings at the
cost of higher power usage.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **viewport\_get\_render\_info**(viewport:
`RID<class_RID>`, type:
`ViewportRenderInfoType<enum_RenderingServer_ViewportRenderInfoType>`,
info: `ViewportRenderInfo<enum_RenderingServer_ViewportRenderInfo>`)
`🔗<class_RenderingServer_method_viewport_get_render_info>`

Returns a statistic about the rendering engine which can be used for
performance profiling. This is separated into render pass `type`s, each
of them having the same `info`s you can query (different passes will
return different values). See
`ViewportRenderInfoType<enum_RenderingServer_ViewportRenderInfoType>`
for a list of render pass types and
`ViewportRenderInfo<enum_RenderingServer_ViewportRenderInfo>` for a list
of information that can be queried.

See also
`get_rendering_info<class_RenderingServer_method_get_rendering_info>`,
which returns global information across all viewports.

\*\*Note:\*\* Viewport rendering information is not available until at
least 2 frames have been rendered by the engine. If rendering
information is not available,
`viewport_get_render_info<class_RenderingServer_method_viewport_get_render_info>`
returns `0`. To print rendering information in `_ready()` successfully,
use the following:

    func _ready():
        for _i in 2:
            await get_tree().process_frame

        print(
                RenderingServer.viewport_get_render_info(get_viewport().get_viewport_rid(),
                RenderingServer.VIEWPORT_RENDER_INFO_TYPE_VISIBLE,
                RenderingServer.VIEWPORT_RENDER_INFO_DRAW_CALLS_IN_FRAME)
        )

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **viewport\_get\_render\_target**(viewport:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_viewport_get_render_target>`

Returns the render target for the viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **viewport\_get\_texture**(viewport: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_viewport_get_texture>`

Returns the viewport's last rendered frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>`
**viewport\_get\_update\_mode**(viewport: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_viewport_get_update_mode>`

Returns the viewport's update mode. See
`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>` constants
for options.

\*\*Warning:\*\* Calling this from any thread other than the rendering
thread will be detrimental to performance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_remove\_canvas**(viewport:
`RID<class_RID>`, canvas: `RID<class_RID>`)
`🔗<class_RenderingServer_method_viewport_remove_canvas>`

Detaches a viewport from a canvas.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_active**(viewport:
`RID<class_RID>`, active: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_active>`

If `true`, sets the viewport active, else sets it inactive.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_canvas\_cull\_mask**(viewport: `RID<class_RID>`,
canvas\_cull\_mask: `int<class_int>`)
`🔗<class_RenderingServer_method_viewport_set_canvas_cull_mask>`

Sets the rendering mask associated with this `Viewport<class_Viewport>`.
Only `CanvasItem<class_CanvasItem>` nodes with a matching rendering
visibility layer will be rendered by this `Viewport<class_Viewport>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_canvas\_stacking**(viewport:
`RID<class_RID>`, canvas: `RID<class_RID>`, layer: `int<class_int>`,
sublayer: `int<class_int>`)
`🔗<class_RenderingServer_method_viewport_set_canvas_stacking>`

Sets the stacking order for a viewport's canvas.

`layer` is the actual canvas layer, while `sublayer` specifies the
stacking order of the canvas among those in the same layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_canvas\_transform**(viewport:
`RID<class_RID>`, canvas: `RID<class_RID>`, offset:
`Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_viewport_set_canvas_transform>`

Sets the transformation of a viewport's canvas.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_clear\_mode**(viewport:
`RID<class_RID>`, clear\_mode:
`ViewportClearMode<enum_RenderingServer_ViewportClearMode>`)
`🔗<class_RenderingServer_method_viewport_set_clear_mode>`

Sets the clear mode of a viewport. See
`ViewportClearMode<enum_RenderingServer_ViewportClearMode>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_debug\_draw**(viewport:
`RID<class_RID>`, draw:
`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>`)
`🔗<class_RenderingServer_method_viewport_set_debug_draw>`

Sets the debug draw mode of a viewport. See
`ViewportDebugDraw<enum_RenderingServer_ViewportDebugDraw>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_default\_canvas\_item\_texture\_filter**(viewport:
`RID<class_RID>`, filter:
`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`)
`🔗<class_RenderingServer_method_viewport_set_default_canvas_item_texture_filter>`

Sets the default texture filtering mode for the specified `viewport`
RID. See
`CanvasItemTextureFilter<enum_RenderingServer_CanvasItemTextureFilter>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_default\_canvas\_item\_texture\_repeat**(viewport:
`RID<class_RID>`, repeat:
`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`)
`🔗<class_RenderingServer_method_viewport_set_default_canvas_item_texture_repeat>`

Sets the default texture repeat mode for the specified `viewport` RID.
See
`CanvasItemTextureRepeat<enum_RenderingServer_CanvasItemTextureRepeat>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_disable\_2d**(viewport:
`RID<class_RID>`, disable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_disable_2d>`

If `true`, the viewport's canvas (i.e. 2D and GUI elements) is not
rendered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_disable\_3d**(viewport:
`RID<class_RID>`, disable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_disable_3d>`

If `true`, the viewport's 3D elements are not rendered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_environment\_mode**(viewport:
`RID<class_RID>`, mode:
`ViewportEnvironmentMode<enum_RenderingServer_ViewportEnvironmentMode>`)
`🔗<class_RenderingServer_method_viewport_set_environment_mode>`

Sets the viewport's environment mode which allows enabling or disabling
rendering of 3D environment over 2D canvas. When disabled, 2D will not
be affected by the environment. When enabled, 2D will be affected by the
environment if the environment background mode is
`ENV_BG_CANVAS<class_RenderingServer_constant_ENV_BG_CANVAS>`. The
default behavior is to inherit the setting from the viewport's parent.
If the topmost parent is also set to
`VIEWPORT_ENVIRONMENT_INHERIT<class_RenderingServer_constant_VIEWPORT_ENVIRONMENT_INHERIT>`,
then the behavior will be the same as if it was set to
`VIEWPORT_ENVIRONMENT_ENABLED<class_RenderingServer_constant_VIEWPORT_ENVIRONMENT_ENABLED>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_fsr\_sharpness**(viewport:
`RID<class_RID>`, sharpness: `float<class_float>`)
`🔗<class_RenderingServer_method_viewport_set_fsr_sharpness>`

Determines how sharp the upscaled image will be when using the FSR
upscaling mode. Sharpness halves with every whole number. Values go from
0.0 (sharpest) to 2.0. Values above 2.0 won't make a visible difference.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_global\_canvas\_transform**(viewport: `RID<class_RID>`,
transform: `Transform2D<class_Transform2D>`)
`🔗<class_RenderingServer_method_viewport_set_global_canvas_transform>`

Sets the viewport's global transformation matrix.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_measure\_render\_time**(viewport: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_measure_render_time>`

Sets the measurement for the given `viewport` RID (obtained using
`Viewport.get_viewport_rid<class_Viewport_method_get_viewport_rid>`).
Once enabled,
`viewport_get_measured_render_time_cpu<class_RenderingServer_method_viewport_get_measured_render_time_cpu>`
and
`viewport_get_measured_render_time_gpu<class_RenderingServer_method_viewport_get_measured_render_time_gpu>`
will return values greater than `0.0` when queried with the given
`viewport`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_msaa\_2d**(viewport:
`RID<class_RID>`, msaa:
`ViewportMSAA<enum_RenderingServer_ViewportMSAA>`)
`🔗<class_RenderingServer_method_viewport_set_msaa_2d>`

Sets the multisample anti-aliasing mode for 2D/Canvas on the specified
`viewport` RID. See `ViewportMSAA<enum_RenderingServer_ViewportMSAA>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_msaa\_3d**(viewport:
`RID<class_RID>`, msaa:
`ViewportMSAA<enum_RenderingServer_ViewportMSAA>`)
`🔗<class_RenderingServer_method_viewport_set_msaa_3d>`

Sets the multisample anti-aliasing mode for 3D on the specified
`viewport` RID. See `ViewportMSAA<enum_RenderingServer_ViewportMSAA>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_occlusion\_culling\_build\_quality**(quality:
`ViewportOcclusionCullingBuildQuality<enum_RenderingServer_ViewportOcclusionCullingBuildQuality>`)
`🔗<class_RenderingServer_method_viewport_set_occlusion_culling_build_quality>`

Sets the
`ProjectSettings.rendering/occlusion_culling/bvh_build_quality<class_ProjectSettings_property_rendering/occlusion_culling/bvh_build_quality>`
to use for occlusion culling. This parameter is global and cannot be set
on a per-viewport basis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_occlusion\_rays\_per\_thread**(rays\_per\_thread:
`int<class_int>`)
`🔗<class_RenderingServer_method_viewport_set_occlusion_rays_per_thread>`

Sets the
`ProjectSettings.rendering/occlusion_culling/occlusion_rays_per_thread<class_ProjectSettings_property_rendering/occlusion_culling/occlusion_rays_per_thread>`
to use for occlusion culling. This parameter is global and cannot be set
on a per-viewport basis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_parent\_viewport**(viewport:
`RID<class_RID>`, parent\_viewport: `RID<class_RID>`)
`🔗<class_RenderingServer_method_viewport_set_parent_viewport>`

Sets the viewport's parent to the viewport specified by the
`parent_viewport` RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_positional\_shadow\_atlas\_quadrant\_subdivision**(viewport:
`RID<class_RID>`, quadrant: `int<class_int>`, subdivision:
`int<class_int>`)
`🔗<class_RenderingServer_method_viewport_set_positional_shadow_atlas_quadrant_subdivision>`

Sets the number of subdivisions to use in the specified shadow atlas
`quadrant` for omni and spot shadows. See also
`Viewport.set_positional_shadow_atlas_quadrant_subdiv<class_Viewport_method_set_positional_shadow_atlas_quadrant_subdiv>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_positional\_shadow\_atlas\_size**(viewport:
`RID<class_RID>`, size: `int<class_int>`, use\_16\_bits:
`bool<class_bool>` = false)
`🔗<class_RenderingServer_method_viewport_set_positional_shadow_atlas_size>`

Sets the `size` of the shadow atlas's images (used for omni and spot
lights) on the viewport specified by the `viewport` RID. The value is
rounded up to the nearest power of 2. If `use_16_bits` is `true`, use 16
bits for the omni/spot shadow depth map. Enabling this results in
shadows having less precision and may result in shadow acne, but can
lead to performance improvements on some devices.

\*\*Note:\*\* If this is set to `0`, no positional shadows will be
visible at all. This can improve performance significantly on low-end
systems by reducing both the CPU and GPU load (as fewer draw calls are
needed to draw the scene without shadows).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_render\_direct\_to\_screen**(viewport:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_render_direct_to_screen>`

If `true`, render the contents of the viewport directly to screen. This
allows a low-level optimization where you can skip drawing a viewport to
the root viewport. While this optimization can result in a significant
increase in speed (especially on older devices), it comes at a cost of
usability. When this is enabled, you cannot read from the viewport or
from the screen\_texture. You also lose the benefit of certain window
settings, such as the various stretch modes. Another consequence to be
aware of is that in 2D the rendering happens in window coordinates, so
if you have a viewport that is double the size of the window, and you
set this, then only the portion that fits within the window will be
drawn, no automatic scaling is possible, even if your game scene is
significantly larger than the window size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_scaling\_3d\_mode**(viewport:
`RID<class_RID>`, scaling\_3d\_mode:
`ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`)
`🔗<class_RenderingServer_method_viewport_set_scaling_3d_mode>`

Sets the 3D resolution scaling mode. Bilinear scaling renders at
different resolution to either undersample or supersample the viewport.
FidelityFX Super Resolution 1.0, abbreviated to FSR, is an upscaling
technology that produces high quality images at fast framerates by using
a spatially aware upscaling algorithm. FSR is slightly more expensive
than bilinear, but it produces significantly higher image quality. FSR
should be used where possible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_scaling\_3d\_scale**(viewport: `RID<class_RID>`, scale:
`float<class_float>`)
`🔗<class_RenderingServer_method_viewport_set_scaling_3d_scale>`

Scales the 3D render buffer based on the viewport size uses an image
filter specified in
`ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>` to
scale the output image to the full viewport size. Values lower than
`1.0` can be used to speed up 3D rendering at the cost of quality
(undersampling). Values greater than `1.0` are only valid for bilinear
mode and can be used to improve 3D rendering quality at a high
performance cost (supersampling). See also
`ViewportMSAA<enum_RenderingServer_ViewportMSAA>` for multi-sample
antialiasing, which is significantly cheaper but only smoothens the
edges of polygons.

When using FSR upscaling, AMD recommends exposing the following values
as preset options to users "Ultra Quality: 0.77", "Quality: 0.67",
"Balanced: 0.59", "Performance: 0.5" instead of exposing the entire
scale.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_scenario**(viewport:
`RID<class_RID>`, scenario: `RID<class_RID>`)
`🔗<class_RenderingServer_method_viewport_set_scenario>`

Sets a viewport's scenario. The scenario contains information about
environment information, reflection atlas, etc.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_screen\_space\_aa**(viewport:
`RID<class_RID>`, mode:
`ViewportScreenSpaceAA<enum_RenderingServer_ViewportScreenSpaceAA>`)
`🔗<class_RenderingServer_method_viewport_set_screen_space_aa>`

Sets the viewport's screen-space antialiasing mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_sdf\_oversize\_and\_scale**(viewport: `RID<class_RID>`,
oversize:
`ViewportSDFOversize<enum_RenderingServer_ViewportSDFOversize>`, scale:
`ViewportSDFScale<enum_RenderingServer_ViewportSDFScale>`)
`🔗<class_RenderingServer_method_viewport_set_sdf_oversize_and_scale>`

Sets the viewport's 2D signed distance field
`ProjectSettings.rendering/2d/sdf/oversize<class_ProjectSettings_property_rendering/2d/sdf/oversize>`
and
`ProjectSettings.rendering/2d/sdf/scale<class_ProjectSettings_property_rendering/2d/sdf/scale>`.
This is used when sampling the signed distance field in
`CanvasItem<class_CanvasItem>` shaders as well as
`GPUParticles2D<class_GPUParticles2D>` collision. This is *not* used by
SDFGI in 3D rendering.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_size**(viewport:
`RID<class_RID>`, width: `int<class_int>`, height: `int<class_int>`)
`🔗<class_RenderingServer_method_viewport_set_size>`

Sets the viewport's width and height in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_snap\_2d\_transforms\_to\_pixel**(viewport:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_snap_2d_transforms_to_pixel>`

If `true`, canvas item transforms (i.e. origin position) are snapped to
the nearest pixel when rendering. This can lead to a crisper appearance
at the cost of less smooth movement, especially when
`Camera2D<class_Camera2D>` smoothing is enabled. Equivalent to
`ProjectSettings.rendering/2d/snap/snap_2d_transforms_to_pixel<class_ProjectSettings_property_rendering/2d/snap/snap_2d_transforms_to_pixel>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_snap\_2d\_vertices\_to\_pixel**(viewport:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_snap_2d_vertices_to_pixel>`

If `true`, canvas item vertices (i.e. polygon points) are snapped to the
nearest pixel when rendering. This can lead to a crisper appearance at
the cost of less smooth movement, especially when
`Camera2D<class_Camera2D>` smoothing is enabled. Equivalent to
`ProjectSettings.rendering/2d/snap/snap_2d_vertices_to_pixel<class_ProjectSettings_property_rendering/2d/snap/snap_2d_vertices_to_pixel>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_texture\_mipmap\_bias**(viewport: `RID<class_RID>`,
mipmap\_bias: `float<class_float>`)
`🔗<class_RenderingServer_method_viewport_set_texture_mipmap_bias>`

Affects the final texture sharpness by reading from a lower or higher
mipmap (also called "texture LOD bias"). Negative values make mipmapped
textures sharper but grainier when viewed at a distance, while positive
values make mipmapped textures blurrier (even when up close). To get
sharper textures at a distance without introducing too much graininess,
set this between `-0.75` and `0.0`. Enabling temporal antialiasing
(`ProjectSettings.rendering/anti_aliasing/quality/use_taa<class_ProjectSettings_property_rendering/anti_aliasing/quality/use_taa>`)
can help reduce the graininess visible when using negative mipmap bias.

\*\*Note:\*\* When the 3D scaling mode is set to FSR 1.0, this value is
used to adjust the automatic mipmap bias which is calculated internally
based on the scale factor. The formula for this is
`-log2(1.0 / scale) + mipmap_bias`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_transparent\_background**(viewport: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_transparent_background>`

If `true`, the viewport renders its background as transparent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_update\_mode**(viewport:
`RID<class_RID>`, update\_mode:
`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>`)
`🔗<class_RenderingServer_method_viewport_set_update_mode>`

Sets when the viewport should be updated. See
`ViewportUpdateMode<enum_RenderingServer_ViewportUpdateMode>` constants
for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_use\_debanding**(viewport:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_use_debanding>`

If `true`, enables debanding on the specified viewport. Equivalent to
`ProjectSettings.rendering/anti_aliasing/quality/use_debanding<class_ProjectSettings_property_rendering/anti_aliasing/quality/use_debanding>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_use\_hdr\_2d**(viewport:
`RID<class_RID>`, enabled: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_use_hdr_2d>`

If `true`, 2D rendering will use a high dynamic range (HDR) format
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
effects requiring highly detailed gradients. This setting has the same
effect as `Viewport.use_hdr_2d<class_Viewport_property_use_hdr_2d>`.

\*\*Note:\*\* This setting will have no effect when using the GL
Compatibility renderer as the GL Compatibility renderer always renders
in low dynamic range for performance reasons.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**viewport\_set\_use\_occlusion\_culling**(viewport: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_use_occlusion_culling>`

If `true`, enables occlusion culling on the specified viewport.
Equivalent to
`ProjectSettings.rendering/occlusion_culling/use_occlusion_culling<class_ProjectSettings_property_rendering/occlusion_culling/use_occlusion_culling>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_use\_taa**(viewport:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_use_taa>`

If `true`, use Temporal Anti-Aliasing. Equivalent to
`ProjectSettings.rendering/anti_aliasing/quality/use_taa<class_ProjectSettings_property_rendering/anti_aliasing/quality/use_taa>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_use\_xr**(viewport:
`RID<class_RID>`, use\_xr: `bool<class_bool>`)
`🔗<class_RenderingServer_method_viewport_set_use_xr>`

If `true`, the viewport uses augmented or virtual reality technologies.
See `XRInterface<class_XRInterface>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_vrs\_mode**(viewport:
`RID<class_RID>`, mode:
`ViewportVRSMode<enum_RenderingServer_ViewportVRSMode>`)
`🔗<class_RenderingServer_method_viewport_set_vrs_mode>`

Sets the Variable Rate Shading (VRS) mode for the viewport. If the GPU
does not support VRS, this property is ignored. Equivalent to
`ProjectSettings.rendering/vrs/mode<class_ProjectSettings_property_rendering/vrs/mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_vrs\_texture**(viewport:
`RID<class_RID>`, texture: `RID<class_RID>`)
`🔗<class_RenderingServer_method_viewport_set_vrs_texture>`

The texture to use when the VRS mode is set to
`VIEWPORT_VRS_TEXTURE<class_RenderingServer_constant_VIEWPORT_VRS_TEXTURE>`.
Equivalent to
`ProjectSettings.rendering/vrs/texture<class_ProjectSettings_property_rendering/vrs/texture>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **viewport\_set\_vrs\_update\_mode**(viewport:
`RID<class_RID>`, mode:
`ViewportVRSUpdateMode<enum_RenderingServer_ViewportVRSUpdateMode>`)
`🔗<class_RenderingServer_method_viewport_set_vrs_update_mode>`

Sets the update mode for Variable Rate Shading (VRS) for the viewport.
VRS requires the input texture to be converted to the format usable by
the VRS method supported by the hardware. The update mode defines how
often this happens. If the GPU does not support VRS, or VRS is not
enabled, this property is ignored.

If set to
`VIEWPORT_VRS_UPDATE_ONCE<class_RenderingServer_constant_VIEWPORT_VRS_UPDATE_ONCE>`,
the input texture is copied once and the mode is changed to
`VIEWPORT_VRS_UPDATE_DISABLED<class_RenderingServer_constant_VIEWPORT_VRS_UPDATE_DISABLED>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **visibility\_notifier\_create**()
`🔗<class_RenderingServer_method_visibility_notifier_create>`

Creates a new 3D visibility notifier object and adds it to the
RenderingServer. It can be accessed with the RID that is returned. This
RID will be used in all `visibility_notifier_*` RenderingServer
functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

To place in a scene, attach this mesh to an instance using
`instance_set_base<class_RenderingServer_method_instance_set_base>`
using the returned RID.

\*\*Note:\*\* The equivalent node is
`VisibleOnScreenNotifier3D<class_VisibleOnScreenNotifier3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **visibility\_notifier\_set\_aabb**(notifier:
`RID<class_RID>`, aabb: `AABB<class_AABB>`)
`🔗<class_RenderingServer_method_visibility_notifier_set_aabb>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**visibility\_notifier\_set\_callbacks**(notifier: `RID<class_RID>`,
enter\_callable: `Callable<class_Callable>`, exit\_callable:
`Callable<class_Callable>`)
`🔗<class_RenderingServer_method_visibility_notifier_set_callbacks>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **voxel\_gi\_allocate\_data**(voxel\_gi:
`RID<class_RID>`, to\_cell\_xform: `Transform3D<class_Transform3D>`,
aabb: `AABB<class_AABB>`, octree\_size: `Vector3i<class_Vector3i>`,
octree\_cells: `PackedByteArray<class_PackedByteArray>`, data\_cells:
`PackedByteArray<class_PackedByteArray>`, distance\_field:
`PackedByteArray<class_PackedByteArray>`, level\_counts:
`PackedInt32Array<class_PackedInt32Array>`)
`🔗<class_RenderingServer_method_voxel_gi_allocate_data>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **voxel\_gi\_create**()
`🔗<class_RenderingServer_method_voxel_gi_create>`

Creates a new voxel-based global illumination object and adds it to the
RenderingServer. It can be accessed with the RID that is returned. This
RID will be used in all `voxel_gi_*` RenderingServer functions.

Once finished with your RID, you will want to free the RID using the
RenderingServer's `free_rid<class_RenderingServer_method_free_rid>`
method.

\*\*Note:\*\* The equivalent node is `VoxelGI<class_VoxelGI>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**voxel\_gi\_get\_data\_cells**(voxel\_gi: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_voxel_gi_get_data_cells>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**voxel\_gi\_get\_distance\_field**(voxel\_gi: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_voxel_gi_get_distance_field>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**voxel\_gi\_get\_level\_counts**(voxel\_gi: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_voxel_gi_get_level_counts>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**voxel\_gi\_get\_octree\_cells**(voxel\_gi: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_voxel_gi_get_octree_cells>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3i<class_Vector3i>` **voxel\_gi\_get\_octree\_size**(voxel\_gi:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_voxel_gi_get_octree_size>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>`
**voxel\_gi\_get\_to\_cell\_xform**(voxel\_gi: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingServer_method_voxel_gi_get_to_cell_xform>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**voxel\_gi\_set\_baked\_exposure\_normalization**(voxel\_gi:
`RID<class_RID>`, baked\_exposure: `float<class_float>`)
`🔗<class_RenderingServer_method_voxel_gi_set_baked_exposure_normalization>`

Used to inform the renderer what exposure normalization value was used
while baking the voxel gi. This value will be used and modulated at run
time to ensure that the voxel gi maintains a consistent level of
exposure even if the scene-wide exposure normalization is changed at run
time. For more information see
`camera_attributes_set_exposure<class_RenderingServer_method_camera_attributes_set_exposure>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **voxel\_gi\_set\_bias**(voxel\_gi:
`RID<class_RID>`, bias: `float<class_float>`)
`🔗<class_RenderingServer_method_voxel_gi_set_bias>`

Sets the `VoxelGIData.bias<class_VoxelGIData_property_bias>` value to
use on the specified `voxel_gi`'s `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **voxel\_gi\_set\_dynamic\_range**(voxel\_gi:
`RID<class_RID>`, range: `float<class_float>`)
`🔗<class_RenderingServer_method_voxel_gi_set_dynamic_range>`

Sets the
`VoxelGIData.dynamic_range<class_VoxelGIData_property_dynamic_range>`
value to use on the specified `voxel_gi`'s `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **voxel\_gi\_set\_energy**(voxel\_gi:
`RID<class_RID>`, energy: `float<class_float>`)
`🔗<class_RenderingServer_method_voxel_gi_set_energy>`

Sets the `VoxelGIData.energy<class_VoxelGIData_property_energy>` value
to use on the specified `voxel_gi`'s `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **voxel\_gi\_set\_interior**(voxel\_gi:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_voxel_gi_set_interior>`

Sets the `VoxelGIData.interior<class_VoxelGIData_property_interior>`
value to use on the specified `voxel_gi`'s `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **voxel\_gi\_set\_normal\_bias**(voxel\_gi:
`RID<class_RID>`, bias: `float<class_float>`)
`🔗<class_RenderingServer_method_voxel_gi_set_normal_bias>`

Sets the
`VoxelGIData.normal_bias<class_VoxelGIData_property_normal_bias>` value
to use on the specified `voxel_gi`'s `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **voxel\_gi\_set\_propagation**(voxel\_gi:
`RID<class_RID>`, amount: `float<class_float>`)
`🔗<class_RenderingServer_method_voxel_gi_set_propagation>`

Sets the
`VoxelGIData.propagation<class_VoxelGIData_property_propagation>` value
to use on the specified `voxel_gi`'s `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **voxel\_gi\_set\_quality**(quality:
`VoxelGIQuality<enum_RenderingServer_VoxelGIQuality>`)
`🔗<class_RenderingServer_method_voxel_gi_set_quality>`

Sets the
`ProjectSettings.rendering/global_illumination/voxel_gi/quality<class_ProjectSettings_property_rendering/global_illumination/voxel_gi/quality>`
value to use when rendering. This parameter is global and cannot be set
on a per-VoxelGI basis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**voxel\_gi\_set\_use\_two\_bounces**(voxel\_gi: `RID<class_RID>`,
enable: `bool<class_bool>`)
`🔗<class_RenderingServer_method_voxel_gi_set_use_two_bounces>`

Sets the
`VoxelGIData.use_two_bounces<class_VoxelGIData_property_use_two_bounces>`
value to use on the specified `voxel_gi`'s `RID<class_RID>`.
