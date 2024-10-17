github\_url  
hide

# RenderingDevice

**Inherits:** `Object<class_Object>`

Abstraction for working with modern low-level graphics APIs.

classref-introduction-group

## Description

**RenderingDevice** is an abstraction for working with modern low-level
graphics APIs such as Vulkan. Compared to
`RenderingServer<class_RenderingServer>` (which works with Godot's own
rendering subsystems), **RenderingDevice** is much lower-level and
allows working more directly with the underlying graphics APIs.
**RenderingDevice** is used in Godot to provide support for several
modern low-level graphics APIs while reducing the amount of code
duplication required. **RenderingDevice** can also be used in your own
projects to perform things that are not exposed by
`RenderingServer<class_RenderingServer>` or high-level nodes, such as
using compute shaders.

On startup, Godot creates a global **RenderingDevice** which can be
retrieved using
`RenderingServer.get_rendering_device<class_RenderingServer_method_get_rendering_device>`.
This global **RenderingDevice** performs drawing to the screen.

\*\*Local RenderingDevices:\*\* Using
`RenderingServer.create_local_rendering_device<class_RenderingServer_method_create_local_rendering_device>`,
you can create "secondary" rendering devices to perform drawing and GPU
compute operations on separate threads.

\*\*Note:\*\* **RenderingDevice** assumes intermediate knowledge of
modern graphics APIs such as Vulkan, Direct3D 12, Metal or WebGPU. These
graphics APIs are lower-level than OpenGL or Direct3D 11, requiring you
to perform what was previously done by the graphics driver itself. If
you have difficulty understanding the concepts used in this class,
follow the [Vulkan Tutorial](https://vulkan-tutorial.com/) or [Vulkan
Guide](https://vkguide.dev/). It's recommended to have existing modern
OpenGL or Direct3D 11 knowledge before attempting to learn a low-level
graphics API.

\*\*Note:\*\* **RenderingDevice** is not available when running in
headless mode or when using the Compatibility rendering method.

classref-introduction-group

## Tutorials

-   `Using compute shaders <../tutorials/shaders/compute_shaders>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **DeviceType**: `🔗<enum_RenderingDevice_DeviceType>`

classref-enumeration-constant

`DeviceType<enum_RenderingDevice_DeviceType>` **DEVICE\_TYPE\_OTHER** =
`0`

Rendering device type does not match any of the other enum values or is
unknown.

classref-enumeration-constant

`DeviceType<enum_RenderingDevice_DeviceType>`
**DEVICE\_TYPE\_INTEGRATED\_GPU** = `1`

Rendering device is an integrated GPU, which is typically *(but not
always)* slower than dedicated GPUs
(`DEVICE_TYPE_DISCRETE_GPU<class_RenderingDevice_constant_DEVICE_TYPE_DISCRETE_GPU>`).
On Android and iOS, the rendering device type is always considered to be
`DEVICE_TYPE_INTEGRATED_GPU<class_RenderingDevice_constant_DEVICE_TYPE_INTEGRATED_GPU>`.

classref-enumeration-constant

`DeviceType<enum_RenderingDevice_DeviceType>`
**DEVICE\_TYPE\_DISCRETE\_GPU** = `2`

Rendering device is a dedicated GPU, which is typically *(but not
always)* faster than integrated GPUs
(`DEVICE_TYPE_INTEGRATED_GPU<class_RenderingDevice_constant_DEVICE_TYPE_INTEGRATED_GPU>`).

classref-enumeration-constant

`DeviceType<enum_RenderingDevice_DeviceType>`
**DEVICE\_TYPE\_VIRTUAL\_GPU** = `3`

Rendering device is an emulated GPU in a virtual environment. This is
typically much slower than the host GPU, which means the expected
performance level on a dedicated GPU will be roughly equivalent to
`DEVICE_TYPE_INTEGRATED_GPU<class_RenderingDevice_constant_DEVICE_TYPE_INTEGRATED_GPU>`.
Virtual machine GPU passthrough (such as VFIO) will not report the
device type as
`DEVICE_TYPE_VIRTUAL_GPU<class_RenderingDevice_constant_DEVICE_TYPE_VIRTUAL_GPU>`.
Instead, the host GPU's device type will be reported as if the GPU was
not emulated.

classref-enumeration-constant

`DeviceType<enum_RenderingDevice_DeviceType>` **DEVICE\_TYPE\_CPU** =
`4`

Rendering device is provided by software emulation (such as Lavapipe or
[SwiftShader](https://github.com/google/swiftshader)). This is the
slowest kind of rendering device available; it's typically much slower
than
`DEVICE_TYPE_INTEGRATED_GPU<class_RenderingDevice_constant_DEVICE_TYPE_INTEGRATED_GPU>`.

classref-enumeration-constant

`DeviceType<enum_RenderingDevice_DeviceType>` **DEVICE\_TYPE\_MAX** =
`5`

Represents the size of the `DeviceType<enum_RenderingDevice_DeviceType>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DriverResource**: `🔗<enum_RenderingDevice_DriverResource>`

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_LOGICAL\_DEVICE** = `0`

Specific device object based on a physical device.

-   Vulkan: Vulkan device driver resource (`VkDevice`). (`rid` argument
    doesn't apply.)

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_PHYSICAL\_DEVICE** = `1`

Physical device the specific logical device is based on.

-   Vulkan: `VkDevice`. (`rid` argument doesn't apply.)

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_TOPMOST\_OBJECT** = `2`

Top-most graphics API entry object.

-   Vulkan: `VkInstance`. (`rid` argument doesn't apply.)

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_COMMAND\_QUEUE** = `3`

The main graphics-compute command queue.

-   Vulkan: `VkQueue`. (`rid` argument doesn't apply.)

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_QUEUE\_FAMILY** = `4`

The specific family the main queue belongs to.

-   Vulkan: the queue family index, an `uint32_t`. (`rid` argument
    doesn't apply.)

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_TEXTURE** = `5`

-   Vulkan: `VkImage`.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_TEXTURE\_VIEW** = `6`

The view of an owned or shared texture.

-   Vulkan: `VkImageView`.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_TEXTURE\_DATA\_FORMAT** = `7`

The native id of the data format of the texture.

-   Vulkan: `VkFormat`.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_SAMPLER** = `8`

-   Vulkan: `VkSampler`.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_UNIFORM\_SET** = `9`

-   Vulkan: `VkDescriptorSet`.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_BUFFER** = `10`

Buffer of any kind of (storage, vertex, etc.).

-   Vulkan: `VkBuffer`.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_COMPUTE\_PIPELINE** = `11`

-   Vulkan: `VkPipeline`.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_RENDER\_PIPELINE** = `12`

-   Vulkan: `VkPipeline`.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_DEVICE** = `0`

**Deprecated:** Use
`DRIVER_RESOURCE_LOGICAL_DEVICE<class_RenderingDevice_constant_DRIVER_RESOURCE_LOGICAL_DEVICE>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_PHYSICAL\_DEVICE** = `1`

**Deprecated:** Use
`DRIVER_RESOURCE_PHYSICAL_DEVICE<class_RenderingDevice_constant_DRIVER_RESOURCE_PHYSICAL_DEVICE>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_INSTANCE** = `2`

**Deprecated:** Use
`DRIVER_RESOURCE_TOPMOST_OBJECT<class_RenderingDevice_constant_DRIVER_RESOURCE_TOPMOST_OBJECT>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_QUEUE** = `3`

**Deprecated:** Use
`DRIVER_RESOURCE_COMMAND_QUEUE<class_RenderingDevice_constant_DRIVER_RESOURCE_COMMAND_QUEUE>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_QUEUE\_FAMILY\_INDEX** = `4`

**Deprecated:** Use
`DRIVER_RESOURCE_QUEUE_FAMILY<class_RenderingDevice_constant_DRIVER_RESOURCE_QUEUE_FAMILY>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_IMAGE** = `5`

**Deprecated:** Use
`DRIVER_RESOURCE_TEXTURE<class_RenderingDevice_constant_DRIVER_RESOURCE_TEXTURE>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_IMAGE\_VIEW** = `6`

**Deprecated:** Use
`DRIVER_RESOURCE_TEXTURE_VIEW<class_RenderingDevice_constant_DRIVER_RESOURCE_TEXTURE_VIEW>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_IMAGE\_NATIVE\_TEXTURE\_FORMAT** = `7`

**Deprecated:** Use
`DRIVER_RESOURCE_TEXTURE_DATA_FORMAT<class_RenderingDevice_constant_DRIVER_RESOURCE_TEXTURE_DATA_FORMAT>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_SAMPLER** = `8`

**Deprecated:** Use
`DRIVER_RESOURCE_SAMPLER<class_RenderingDevice_constant_DRIVER_RESOURCE_SAMPLER>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_DESCRIPTOR\_SET** = `9`

**Deprecated:** Use
`DRIVER_RESOURCE_UNIFORM_SET<class_RenderingDevice_constant_DRIVER_RESOURCE_UNIFORM_SET>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_BUFFER** = `10`

**Deprecated:** Use
`DRIVER_RESOURCE_BUFFER<class_RenderingDevice_constant_DRIVER_RESOURCE_BUFFER>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_COMPUTE\_PIPELINE** = `11`

**Deprecated:** Use
`DRIVER_RESOURCE_COMPUTE_PIPELINE<class_RenderingDevice_constant_DRIVER_RESOURCE_COMPUTE_PIPELINE>`
instead.

classref-enumeration-constant

`DriverResource<enum_RenderingDevice_DriverResource>`
**DRIVER\_RESOURCE\_VULKAN\_RENDER\_PIPELINE** = `12`

**Deprecated:** Use
`DRIVER_RESOURCE_RENDER_PIPELINE<class_RenderingDevice_constant_DRIVER_RESOURCE_RENDER_PIPELINE>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DataFormat**: `🔗<enum_RenderingDevice_DataFormat>`

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R4G4\_UNORM\_PACK8** = `0`

4-bit-per-channel red/green channel data format, packed into 8 bits.
Values are in the `[0.0, 1.0]` range.

\*\*Note:\*\* More information on all data formats can be found on the
[Identification of
formats](https://registry.khronos.org/vulkan/specs/1.1/html/vkspec.html#_identification_of_formats)
section of the Vulkan specification, as well as the
[VkFormat](https://registry.khronos.org/vulkan/specs/1.3-extensions/man/html/VkFormat.html)
enum.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R4G4B4A4\_UNORM\_PACK16** = `1`

4-bit-per-channel red/green/blue/alpha channel data format, packed into
16 bits. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B4G4R4A4\_UNORM\_PACK16** = `2`

4-bit-per-channel blue/green/red/alpha channel data format, packed into
16 bits. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R5G6B5\_UNORM\_PACK16** = `3`

Red/green/blue channel data format with 5 bits of red, 6 bits of green
and 5 bits of blue, packed into 16 bits. Values are in the `[0.0, 1.0]`
range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B5G6R5\_UNORM\_PACK16** = `4`

Blue/green/red channel data format with 5 bits of blue, 6 bits of green
and 5 bits of red, packed into 16 bits. Values are in the `[0.0, 1.0]`
range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R5G5B5A1\_UNORM\_PACK16** = `5`

Red/green/blue/alpha channel data format with 5 bits of red, 6 bits of
green, 5 bits of blue and 1 bit of alpha, packed into 16 bits. Values
are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B5G5R5A1\_UNORM\_PACK16** = `6`

Blue/green/red/alpha channel data format with 5 bits of blue, 6 bits of
green, 5 bits of red and 1 bit of alpha, packed into 16 bits. Values are
in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A1R5G5B5\_UNORM\_PACK16** = `7`

Alpha/red/green/blue channel data format with 1 bit of alpha, 5 bits of
red, 6 bits of green and 5 bits of blue, packed into 16 bits. Values are
in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8\_UNORM** = `8`

8-bit-per-channel unsigned floating-point red channel data format with
normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8\_SNORM** = `9`

8-bit-per-channel signed floating-point red channel data format with
normalized value. Values are in the `[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8\_USCALED** = `10`

8-bit-per-channel unsigned floating-point red channel data format with
scaled value (value is converted from integer to float). Values are in
the `[0.0, 255.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8\_SSCALED** = `11`

8-bit-per-channel signed floating-point red channel data format with
scaled value (value is converted from integer to float). Values are in
the `[-127.0, 127.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>` **DATA\_FORMAT\_R8\_UINT**
= `12`

8-bit-per-channel unsigned integer red channel data format. Values are
in the `[0, 255]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>` **DATA\_FORMAT\_R8\_SINT**
= `13`

8-bit-per-channel signed integer red channel data format. Values are in
the `[-127, 127]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>` **DATA\_FORMAT\_R8\_SRGB**
= `14`

8-bit-per-channel unsigned floating-point red channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8\_UNORM** = `15`

8-bit-per-channel unsigned floating-point red/green channel data format
with normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8\_SNORM** = `16`

8-bit-per-channel signed floating-point red/green channel data format
with normalized value. Values are in the `[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8\_USCALED** = `17`

8-bit-per-channel unsigned floating-point red/green channel data format
with scaled value (value is converted from integer to float). Values are
in the `[0.0, 255.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8\_SSCALED** = `18`

8-bit-per-channel signed floating-point red/green channel data format
with scaled value (value is converted from integer to float). Values are
in the `[-127.0, 127.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8\_UINT** = `19`

8-bit-per-channel unsigned integer red/green channel data format. Values
are in the `[0, 255]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8\_SINT** = `20`

8-bit-per-channel signed integer red/green channel data format. Values
are in the `[-127, 127]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8\_SRGB** = `21`

8-bit-per-channel unsigned floating-point red/green channel data format
with normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8\_UNORM** = `22`

8-bit-per-channel unsigned floating-point red/green/blue channel data
format with normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8\_SNORM** = `23`

8-bit-per-channel signed floating-point red/green/blue channel data
format with normalized value. Values are in the `[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8\_USCALED** = `24`

8-bit-per-channel unsigned floating-point red/green/blue channel data
format with scaled value (value is converted from integer to float).
Values are in the `[0.0, 255.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8\_SSCALED** = `25`

8-bit-per-channel signed floating-point red/green/blue channel data
format with scaled value (value is converted from integer to float).
Values are in the `[-127.0, 127.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8\_UINT** = `26`

8-bit-per-channel unsigned integer red/green/blue channel data format.
Values are in the `[0, 255]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8\_SINT** = `27`

8-bit-per-channel signed integer red/green/blue channel data format.
Values are in the `[-127, 127]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8\_SRGB** = `28`

8-bit-per-channel unsigned floating-point red/green/blue/blue channel
data format with normalized value and non-linear sRGB encoding. Values
are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8\_UNORM** = `29`

8-bit-per-channel unsigned floating-point blue/green/red channel data
format with normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8\_SNORM** = `30`

8-bit-per-channel signed floating-point blue/green/red channel data
format with normalized value. Values are in the `[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8\_USCALED** = `31`

8-bit-per-channel unsigned floating-point blue/green/red channel data
format with scaled value (value is converted from integer to float).
Values are in the `[0.0, 255.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8\_SSCALED** = `32`

8-bit-per-channel signed floating-point blue/green/red channel data
format with scaled value (value is converted from integer to float).
Values are in the `[-127.0, 127.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8\_UINT** = `33`

8-bit-per-channel unsigned integer blue/green/red channel data format.
Values are in the `[0, 255]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8\_SINT** = `34`

8-bit-per-channel signed integer blue/green/red channel data format.
Values are in the `[-127, 127]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8\_SRGB** = `35`

8-bit-per-channel unsigned floating-point blue/green/red data format
with normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8A8\_UNORM** = `36`

8-bit-per-channel unsigned floating-point red/green/blue/alpha channel
data format with normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8A8\_SNORM** = `37`

8-bit-per-channel signed floating-point red/green/blue/alpha channel
data format with normalized value. Values are in the `[-1.0, 1.0]`
range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8A8\_USCALED** = `38`

8-bit-per-channel unsigned floating-point red/green/blue/alpha channel
data format with scaled value (value is converted from integer to
float). Values are in the `[0.0, 255.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8A8\_SSCALED** = `39`

8-bit-per-channel signed floating-point red/green/blue/alpha channel
data format with scaled value (value is converted from integer to
float). Values are in the `[-127.0, 127.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8A8\_UINT** = `40`

8-bit-per-channel unsigned integer red/green/blue/alpha channel data
format. Values are in the `[0, 255]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8A8\_SINT** = `41`

8-bit-per-channel signed integer red/green/blue/alpha channel data
format. Values are in the `[-127, 127]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R8G8B8A8\_SRGB** = `42`

8-bit-per-channel unsigned floating-point red/green/blue/alpha channel
data format with normalized value and non-linear sRGB encoding. Values
are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8A8\_UNORM** = `43`

8-bit-per-channel unsigned floating-point blue/green/red/alpha channel
data format with normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8A8\_SNORM** = `44`

8-bit-per-channel signed floating-point blue/green/red/alpha channel
data format with normalized value. Values are in the `[-1.0, 1.0]`
range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8A8\_USCALED** = `45`

8-bit-per-channel unsigned floating-point blue/green/red/alpha channel
data format with scaled value (value is converted from integer to
float). Values are in the `[0.0, 255.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8A8\_SSCALED** = `46`

8-bit-per-channel signed floating-point blue/green/red/alpha channel
data format with scaled value (value is converted from integer to
float). Values are in the `[-127.0, 127.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8A8\_UINT** = `47`

8-bit-per-channel unsigned integer blue/green/red/alpha channel data
format. Values are in the `[0, 255]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8A8\_SINT** = `48`

8-bit-per-channel signed integer blue/green/red/alpha channel data
format. Values are in the `[-127, 127]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8A8\_SRGB** = `49`

8-bit-per-channel unsigned floating-point blue/green/red/alpha channel
data format with normalized value and non-linear sRGB encoding. Values
are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A8B8G8R8\_UNORM\_PACK32** = `50`

8-bit-per-channel unsigned floating-point alpha/red/green/blue channel
data format with normalized value, packed in 32 bits. Values are in the
`[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A8B8G8R8\_SNORM\_PACK32** = `51`

8-bit-per-channel signed floating-point alpha/red/green/blue channel
data format with normalized value, packed in 32 bits. Values are in the
`[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A8B8G8R8\_USCALED\_PACK32** = `52`

8-bit-per-channel unsigned floating-point alpha/red/green/blue channel
data format with scaled value (value is converted from integer to
float), packed in 32 bits. Values are in the `[0.0, 255.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A8B8G8R8\_SSCALED\_PACK32** = `53`

8-bit-per-channel signed floating-point alpha/red/green/blue channel
data format with scaled value (value is converted from integer to
float), packed in 32 bits. Values are in the `[-127.0, 127.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A8B8G8R8\_UINT\_PACK32** = `54`

8-bit-per-channel unsigned integer alpha/red/green/blue channel data
format, packed in 32 bits. Values are in the `[0, 255]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A8B8G8R8\_SINT\_PACK32** = `55`

8-bit-per-channel signed integer alpha/red/green/blue channel data
format, packed in 32 bits. Values are in the `[-127, 127]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A8B8G8R8\_SRGB\_PACK32** = `56`

8-bit-per-channel unsigned floating-point alpha/red/green/blue channel
data format with normalized value and non-linear sRGB encoding, packed
in 32 bits. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2R10G10B10\_UNORM\_PACK32** = `57`

Unsigned floating-point alpha/red/green/blue channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of red, 10 bits of green and 10 bits of blue. Values are in the
`[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2R10G10B10\_SNORM\_PACK32** = `58`

Signed floating-point alpha/red/green/blue channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of red, 10 bits of green and 10 bits of blue. Values are in the
`[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2R10G10B10\_USCALED\_PACK32** = `59`

Unsigned floating-point alpha/red/green/blue channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of red, 10 bits of green and 10 bits of blue. Values are in the
`[0.0, 1023.0]` range for red/green/blue and `[0.0, 3.0]` for alpha.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2R10G10B10\_SSCALED\_PACK32** = `60`

Signed floating-point alpha/red/green/blue channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of red, 10 bits of green and 10 bits of blue. Values are in the
`[-511.0, 511.0]` range for red/green/blue and `[-1.0, 1.0]` for alpha.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2R10G10B10\_UINT\_PACK32** = `61`

Unsigned integer alpha/red/green/blue channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of red, 10 bits of green and 10 bits of blue. Values are in the
`[0, 1023]` range for red/green/blue and `[0, 3]` for alpha.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2R10G10B10\_SINT\_PACK32** = `62`

Signed integer alpha/red/green/blue channel data format with normalized
value, packed in 32 bits. Format contains 2 bits of alpha, 10 bits of
red, 10 bits of green and 10 bits of blue. Values are in the
`[-511, 511]` range for red/green/blue and `[-1, 1]` for alpha.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2B10G10R10\_UNORM\_PACK32** = `63`

Unsigned floating-point alpha/blue/green/red channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of blue, 10 bits of green and 10 bits of red. Values are in the
`[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2B10G10R10\_SNORM\_PACK32** = `64`

Signed floating-point alpha/blue/green/red channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of blue, 10 bits of green and 10 bits of red. Values are in the
`[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2B10G10R10\_USCALED\_PACK32** = `65`

Unsigned floating-point alpha/blue/green/red channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of blue, 10 bits of green and 10 bits of red. Values are in the
`[0.0, 1023.0]` range for blue/green/red and `[0.0, 3.0]` for alpha.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2B10G10R10\_SSCALED\_PACK32** = `66`

Signed floating-point alpha/blue/green/red channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of blue, 10 bits of green and 10 bits of red. Values are in the
`[-511.0, 511.0]` range for blue/green/red and `[-1.0, 1.0]` for alpha.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2B10G10R10\_UINT\_PACK32** = `67`

Unsigned integer alpha/blue/green/red channel data format with
normalized value, packed in 32 bits. Format contains 2 bits of alpha, 10
bits of blue, 10 bits of green and 10 bits of red. Values are in the
`[0, 1023]` range for blue/green/red and `[0, 3]` for alpha.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_A2B10G10R10\_SINT\_PACK32** = `68`

Signed integer alpha/blue/green/red channel data format with normalized
value, packed in 32 bits. Format contains 2 bits of alpha, 10 bits of
blue, 10 bits of green and 10 bits of red. Values are in the
`[-511, 511]` range for blue/green/red and `[-1, 1]` for alpha.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16\_UNORM** = `69`

16-bit-per-channel unsigned floating-point red channel data format with
normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16\_SNORM** = `70`

16-bit-per-channel signed floating-point red channel data format with
normalized value. Values are in the `[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16\_USCALED** = `71`

16-bit-per-channel unsigned floating-point red channel data format with
scaled value (value is converted from integer to float). Values are in
the `[0.0, 65535.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16\_SSCALED** = `72`

16-bit-per-channel signed floating-point red channel data format with
scaled value (value is converted from integer to float). Values are in
the `[-32767.0, 32767.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16\_UINT** = `73`

16-bit-per-channel unsigned integer red channel data format. Values are
in the `[0.0, 65535]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16\_SINT** = `74`

16-bit-per-channel signed integer red channel data format. Values are in
the `[-32767, 32767]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16\_SFLOAT** = `75`

16-bit-per-channel signed floating-point red channel data format with
the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16\_UNORM** = `76`

16-bit-per-channel unsigned floating-point red/green channel data format
with normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16\_SNORM** = `77`

16-bit-per-channel signed floating-point red/green channel data format
with normalized value. Values are in the `[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16\_USCALED** = `78`

16-bit-per-channel unsigned floating-point red/green channel data format
with scaled value (value is converted from integer to float). Values are
in the `[0.0, 65535.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16\_SSCALED** = `79`

16-bit-per-channel signed floating-point red/green channel data format
with scaled value (value is converted from integer to float). Values are
in the `[-32767.0, 32767.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16\_UINT** = `80`

16-bit-per-channel unsigned integer red/green channel data format.
Values are in the `[0.0, 65535]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16\_SINT** = `81`

16-bit-per-channel signed integer red/green channel data format. Values
are in the `[-32767, 32767]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16\_SFLOAT** = `82`

16-bit-per-channel signed floating-point red/green channel data format
with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16\_UNORM** = `83`

16-bit-per-channel unsigned floating-point red/green/blue channel data
format with normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16\_SNORM** = `84`

16-bit-per-channel signed floating-point red/green/blue channel data
format with normalized value. Values are in the `[-1.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16\_USCALED** = `85`

16-bit-per-channel unsigned floating-point red/green/blue channel data
format with scaled value (value is converted from integer to float).
Values are in the `[0.0, 65535.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16\_SSCALED** = `86`

16-bit-per-channel signed floating-point red/green/blue channel data
format with scaled value (value is converted from integer to float).
Values are in the `[-32767.0, 32767.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16\_UINT** = `87`

16-bit-per-channel unsigned integer red/green/blue channel data format.
Values are in the `[0.0, 65535]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16\_SINT** = `88`

16-bit-per-channel signed integer red/green/blue channel data format.
Values are in the `[-32767, 32767]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16\_SFLOAT** = `89`

16-bit-per-channel signed floating-point red/green/blue channel data
format with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16A16\_UNORM** = `90`

16-bit-per-channel unsigned floating-point red/green/blue/alpha channel
data format with normalized value. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16A16\_SNORM** = `91`

16-bit-per-channel signed floating-point red/green/blue/alpha channel
data format with normalized value. Values are in the `[-1.0, 1.0]`
range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16A16\_USCALED** = `92`

16-bit-per-channel unsigned floating-point red/green/blue/alpha channel
data format with scaled value (value is converted from integer to
float). Values are in the `[0.0, 65535.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16A16\_SSCALED** = `93`

16-bit-per-channel signed floating-point red/green/blue/alpha channel
data format with scaled value (value is converted from integer to
float). Values are in the `[-32767.0, 32767.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16A16\_UINT** = `94`

16-bit-per-channel unsigned integer red/green/blue/alpha channel data
format. Values are in the `[0.0, 65535]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16A16\_SINT** = `95`

16-bit-per-channel signed integer red/green/blue/alpha channel data
format. Values are in the `[-32767, 32767]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R16G16B16A16\_SFLOAT** = `96`

16-bit-per-channel signed floating-point red/green/blue/alpha channel
data format with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32\_UINT** = `97`

32-bit-per-channel unsigned integer red channel data format. Values are
in the `[0, 2^32 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32\_SINT** = `98`

32-bit-per-channel signed integer red channel data format. Values are in
the `[2^31 + 1, 2^31 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32\_SFLOAT** = `99`

32-bit-per-channel signed floating-point red channel data format with
the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32\_UINT** = `100`

32-bit-per-channel unsigned integer red/green channel data format.
Values are in the `[0, 2^32 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32\_SINT** = `101`

32-bit-per-channel signed integer red/green channel data format. Values
are in the `[2^31 + 1, 2^31 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32\_SFLOAT** = `102`

32-bit-per-channel signed floating-point red/green channel data format
with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32B32\_UINT** = `103`

32-bit-per-channel unsigned integer red/green/blue channel data format.
Values are in the `[0, 2^32 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32B32\_SINT** = `104`

32-bit-per-channel signed integer red/green/blue channel data format.
Values are in the `[2^31 + 1, 2^31 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32B32\_SFLOAT** = `105`

32-bit-per-channel signed floating-point red/green/blue channel data
format with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32B32A32\_UINT** = `106`

32-bit-per-channel unsigned integer red/green/blue/alpha channel data
format. Values are in the `[0, 2^32 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32B32A32\_SINT** = `107`

32-bit-per-channel signed integer red/green/blue/alpha channel data
format. Values are in the `[2^31 + 1, 2^31 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R32G32B32A32\_SFLOAT** = `108`

32-bit-per-channel signed floating-point red/green/blue/alpha channel
data format with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64\_UINT** = `109`

64-bit-per-channel unsigned integer red channel data format. Values are
in the `[0, 2^64 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64\_SINT** = `110`

64-bit-per-channel signed integer red channel data format. Values are in
the `[2^63 + 1, 2^63 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64\_SFLOAT** = `111`

64-bit-per-channel signed floating-point red channel data format with
the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64\_UINT** = `112`

64-bit-per-channel unsigned integer red/green channel data format.
Values are in the `[0, 2^64 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64\_SINT** = `113`

64-bit-per-channel signed integer red/green channel data format. Values
are in the `[2^63 + 1, 2^63 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64\_SFLOAT** = `114`

64-bit-per-channel signed floating-point red/green channel data format
with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64B64\_UINT** = `115`

64-bit-per-channel unsigned integer red/green/blue channel data format.
Values are in the `[0, 2^64 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64B64\_SINT** = `116`

64-bit-per-channel signed integer red/green/blue channel data format.
Values are in the `[2^63 + 1, 2^63 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64B64\_SFLOAT** = `117`

64-bit-per-channel signed floating-point red/green/blue channel data
format with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64B64A64\_UINT** = `118`

64-bit-per-channel unsigned integer red/green/blue/alpha channel data
format. Values are in the `[0, 2^64 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64B64A64\_SINT** = `119`

64-bit-per-channel signed integer red/green/blue/alpha channel data
format. Values are in the `[2^63 + 1, 2^63 - 1]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R64G64B64A64\_SFLOAT** = `120`

64-bit-per-channel signed floating-point red/green/blue/alpha channel
data format with the value stored as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B10G11R11\_UFLOAT\_PACK32** = `121`

Unsigned floating-point blue/green/red data format with the value stored
as-is, packed in 32 bits. The format's precision is 10 bits of blue
channel, 11 bits of green channel and 11 bits of red channel.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_E5B9G9R9\_UFLOAT\_PACK32** = `122`

Unsigned floating-point exposure/blue/green/red data format with the
value stored as-is, packed in 32 bits. The format's precision is 5 bits
of exposure, 9 bits of blue channel, 9 bits of green channel and 9 bits
of red channel.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_D16\_UNORM** = `123`

16-bit unsigned floating-point depth data format with normalized value.
Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_X8\_D24\_UNORM\_PACK32** = `124`

24-bit unsigned floating-point depth data format with normalized value,
plus 8 unused bits, packed in 32 bits. Values for depth are in the
`[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_D32\_SFLOAT** = `125`

32-bit signed floating-point depth data format with the value stored
as-is.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>` **DATA\_FORMAT\_S8\_UINT**
= `126`

8-bit unsigned integer stencil data format.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_D16\_UNORM\_S8\_UINT** = `127`

16-bit unsigned floating-point depth data format with normalized value,
plus 8 bits of stencil in unsigned integer format. Values for depth are
in the `[0.0, 1.0]` range. Values for stencil are in the `[0, 255]`
range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_D24\_UNORM\_S8\_UINT** = `128`

24-bit unsigned floating-point depth data format with normalized value,
plus 8 bits of stencil in unsigned integer format. Values for depth are
in the `[0.0, 1.0]` range. Values for stencil are in the `[0, 255]`
range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_D32\_SFLOAT\_S8\_UINT** = `129`

32-bit signed floating-point depth data format with the value stored
as-is, plus 8 bits of stencil in unsigned integer format. Values for
stencil are in the `[0, 255]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC1\_RGB\_UNORM\_BLOCK** = `130`

VRAM-compressed unsigned red/green/blue channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. The format's
precision is 5 bits of red channel, 6 bits of green channel and 5 bits
of blue channel. Using BC1 texture compression (also known as S3TC
DXT1).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC1\_RGB\_SRGB\_BLOCK** = `131`

VRAM-compressed unsigned red/green/blue channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range. The format's precision is 5 bits of red channel, 6
bits of green channel and 5 bits of blue channel. Using BC1 texture
compression (also known as S3TC DXT1).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC1\_RGBA\_UNORM\_BLOCK** = `132`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. The format's
precision is 5 bits of red channel, 6 bits of green channel, 5 bits of
blue channel and 1 bit of alpha channel. Using BC1 texture compression
(also known as S3TC DXT1).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC1\_RGBA\_SRGB\_BLOCK** = `133`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range. The format's precision is 5 bits of red channel, 6
bits of green channel, 5 bits of blue channel and 1 bit of alpha
channel. Using BC1 texture compression (also known as S3TC DXT1).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC2\_UNORM\_BLOCK** = `134`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. The format's
precision is 5 bits of red channel, 6 bits of green channel, 5 bits of
blue channel and 4 bits of alpha channel. Using BC2 texture compression
(also known as S3TC DXT3).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC2\_SRGB\_BLOCK** = `135`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range. The format's precision is 5 bits of red channel, 6
bits of green channel, 5 bits of blue channel and 4 bits of alpha
channel. Using BC2 texture compression (also known as S3TC DXT3).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC3\_UNORM\_BLOCK** = `136`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. The format's
precision is 5 bits of red channel, 6 bits of green channel, 5 bits of
blue channel and 8 bits of alpha channel. Using BC3 texture compression
(also known as S3TC DXT5).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC3\_SRGB\_BLOCK** = `137`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range. The format's precision is 5 bits of red channel, 6
bits of green channel, 5 bits of blue channel and 8 bits of alpha
channel. Using BC3 texture compression (also known as S3TC DXT5).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC4\_UNORM\_BLOCK** = `138`

VRAM-compressed unsigned red channel data format with normalized value.
Values are in the `[0.0, 1.0]` range. The format's precision is 8 bits
of red channel. Using BC4 texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC4\_SNORM\_BLOCK** = `139`

VRAM-compressed signed red channel data format with normalized value.
Values are in the `[-1.0, 1.0]` range. The format's precision is 8 bits
of red channel. Using BC4 texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC5\_UNORM\_BLOCK** = `140`

VRAM-compressed unsigned red/green channel data format with normalized
value. Values are in the `[0.0, 1.0]` range. The format's precision is 8
bits of red channel and 8 bits of green channel. Using BC5 texture
compression (also known as S3TC RGTC).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC5\_SNORM\_BLOCK** = `141`

VRAM-compressed signed red/green channel data format with normalized
value. Values are in the `[-1.0, 1.0]` range. The format's precision is
8 bits of red channel and 8 bits of green channel. Using BC5 texture
compression (also known as S3TC RGTC).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC6H\_UFLOAT\_BLOCK** = `142`

VRAM-compressed unsigned red/green/blue channel data format with the
floating-point value stored as-is. The format's precision is between 10
and 13 bits for the red/green/blue channels. Using BC6H texture
compression (also known as BPTC HDR).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC6H\_SFLOAT\_BLOCK** = `143`

VRAM-compressed signed red/green/blue channel data format with the
floating-point value stored as-is. The format's precision is between 10
and 13 bits for the red/green/blue channels. Using BC6H texture
compression (also known as BPTC HDR).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC7\_UNORM\_BLOCK** = `144`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. The format's
precision is between 4 and 7 bits for the red/green/blue channels and
between 0 and 8 bits for the alpha channel. Also known as BPTC LDR.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_BC7\_SRGB\_BLOCK** = `145`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range. The format's precision is between 4 and 7 bits for
the red/green/blue channels and between 0 and 8 bits for the alpha
channel. Also known as BPTC LDR.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ETC2\_R8G8B8\_UNORM\_BLOCK** = `146`

VRAM-compressed unsigned red/green/blue channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. Using ETC2
texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ETC2\_R8G8B8\_SRGB\_BLOCK** = `147`

VRAM-compressed unsigned red/green/blue channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range. Using ETC2 texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ETC2\_R8G8B8A1\_UNORM\_BLOCK** = `148`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. Red/green/blue
use 8 bit of precision each, with alpha using 1 bit of precision. Using
ETC2 texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ETC2\_R8G8B8A1\_SRGB\_BLOCK** = `149`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range. Red/green/blue use 8 bit of precision each, with
alpha using 1 bit of precision. Using ETC2 texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ETC2\_R8G8B8A8\_UNORM\_BLOCK** = `150`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. Red/green/blue
use 8 bits of precision each, with alpha using 8 bits of precision.
Using ETC2 texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ETC2\_R8G8B8A8\_SRGB\_BLOCK** = `151`

VRAM-compressed unsigned red/green/blue/alpha channel data format with
normalized value and non-linear sRGB encoding. Values are in the
`[0.0, 1.0]` range. Red/green/blue use 8 bits of precision each, with
alpha using 8 bits of precision. Using ETC2 texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_EAC\_R11\_UNORM\_BLOCK** = `152`

11-bit VRAM-compressed unsigned red channel data format with normalized
value. Values are in the `[0.0, 1.0]` range. Using ETC2 texture
compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_EAC\_R11\_SNORM\_BLOCK** = `153`

11-bit VRAM-compressed signed red channel data format with normalized
value. Values are in the `[-1.0, 1.0]` range. Using ETC2 texture
compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_EAC\_R11G11\_UNORM\_BLOCK** = `154`

11-bit VRAM-compressed unsigned red/green channel data format with
normalized value. Values are in the `[0.0, 1.0]` range. Using ETC2
texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_EAC\_R11G11\_SNORM\_BLOCK** = `155`

11-bit VRAM-compressed signed red/green channel data format with
normalized value. Values are in the `[-1.0, 1.0]` range. Using ETC2
texture compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_4x4\_UNORM\_BLOCK** = `156`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 4×4 blocks (highest quality). Values are in the
`[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_4x4\_SRGB\_BLOCK** = `157`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 4×4 blocks (highest
quality). Values are in the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_5x4\_UNORM\_BLOCK** = `158`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 5×4 blocks. Values are in the `[0.0, 1.0]` range. Using
ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_5x4\_SRGB\_BLOCK** = `159`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 5×4 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_5x5\_UNORM\_BLOCK** = `160`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 5×5 blocks. Values are in the `[0.0, 1.0]` range. Using
ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_5x5\_SRGB\_BLOCK** = `161`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 5×5 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_6x5\_UNORM\_BLOCK** = `162`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 6×5 blocks. Values are in the `[0.0, 1.0]` range. Using
ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_6x5\_SRGB\_BLOCK** = `163`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 6×5 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_6x6\_UNORM\_BLOCK** = `164`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 6×6 blocks. Values are in the `[0.0, 1.0]` range. Using
ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_6x6\_SRGB\_BLOCK** = `165`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 6×6 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_8x5\_UNORM\_BLOCK** = `166`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 8×5 blocks. Values are in the `[0.0, 1.0]` range. Using
ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_8x5\_SRGB\_BLOCK** = `167`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 8×5 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_8x6\_UNORM\_BLOCK** = `168`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 8×6 blocks. Values are in the `[0.0, 1.0]` range. Using
ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_8x6\_SRGB\_BLOCK** = `169`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 8×6 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_8x8\_UNORM\_BLOCK** = `170`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 8×8 blocks. Values are in the `[0.0, 1.0]` range. Using
ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_8x8\_SRGB\_BLOCK** = `171`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 8×8 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_10x5\_UNORM\_BLOCK** = `172`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 10×5 blocks. Values are in the `[0.0, 1.0]` range.
Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_10x5\_SRGB\_BLOCK** = `173`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 10×5 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_10x6\_UNORM\_BLOCK** = `174`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 10×6 blocks. Values are in the `[0.0, 1.0]` range.
Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_10x6\_SRGB\_BLOCK** = `175`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 10×6 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_10x8\_UNORM\_BLOCK** = `176`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 10×8 blocks. Values are in the `[0.0, 1.0]` range.
Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_10x8\_SRGB\_BLOCK** = `177`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 10×8 blocks. Values are in
the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_10x10\_UNORM\_BLOCK** = `178`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 10×10 blocks. Values are in the `[0.0, 1.0]` range.
Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_10x10\_SRGB\_BLOCK** = `179`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 10×10 blocks. Values are
in the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_12x10\_UNORM\_BLOCK** = `180`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 12×10 blocks. Values are in the `[0.0, 1.0]` range.
Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_12x10\_SRGB\_BLOCK** = `181`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 12×10 blocks. Values are
in the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_12x12\_UNORM\_BLOCK** = `182`

VRAM-compressed unsigned floating-point data format with normalized
value, packed in 12 blocks (lowest quality). Values are in the
`[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_ASTC\_12x12\_SRGB\_BLOCK** = `183`

VRAM-compressed unsigned floating-point data format with normalized
value and non-linear sRGB encoding, packed in 12 blocks (lowest
quality). Values are in the `[0.0, 1.0]` range. Using ASTC compression.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G8B8G8R8\_422\_UNORM** = `184`

8-bit-per-channel unsigned floating-point green/blue/red channel data
format with normalized value. Values are in the `[0.0, 1.0]` range. Blue
and red channel data is stored at halved horizontal resolution (i.e. 2
horizontally adjacent pixels will share the same value for the blue/red
channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B8G8R8G8\_422\_UNORM** = `185`

8-bit-per-channel unsigned floating-point blue/green/red channel data
format with normalized value. Values are in the `[0.0, 1.0]` range. Blue
and red channel data is stored at halved horizontal resolution (i.e. 2
horizontally adjacent pixels will share the same value for the blue/red
channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G8\_B8\_R8\_3PLANE\_420\_UNORM** = `186`

8-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, stored across 3 separate planes (green + blue +
red). Values are in the `[0.0, 1.0]` range. Blue and red channel data is
stored at halved horizontal and vertical resolution (i.e. 2×2 adjacent
pixels will share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G8\_B8R8\_2PLANE\_420\_UNORM** = `187`

8-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, stored across 2 separate planes (green +
blue/red). Values are in the `[0.0, 1.0]` range. Blue and red channel
data is stored at halved horizontal and vertical resolution (i.e. 2×2
adjacent pixels will share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G8\_B8\_R8\_3PLANE\_422\_UNORM** = `188`

8-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, stored across 2 separate planes (green + blue +
red). Values are in the `[0.0, 1.0]` range. Blue and red channel data is
stored at halved horizontal resolution (i.e. 2 horizontally adjacent
pixels will share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G8\_B8R8\_2PLANE\_422\_UNORM** = `189`

8-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, stored across 2 separate planes (green +
blue/red). Values are in the `[0.0, 1.0]` range. Blue and red channel
data is stored at halved horizontal resolution (i.e. 2 horizontally
adjacent pixels will share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G8\_B8\_R8\_3PLANE\_444\_UNORM** = `190`

8-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, stored across 3 separate planes. Values are in
the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R10X6\_UNORM\_PACK16** = `191`

10-bit-per-channel unsigned floating-point red channel data with
normalized value, plus 6 unused bits, packed in 16 bits. Values are in
the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R10X6G10X6\_UNORM\_2PACK16** = `192`

10-bit-per-channel unsigned floating-point red/green channel data with
normalized value, plus 6 unused bits after each channel, packed in 2×16
bits. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R10X6G10X6B10X6A10X6\_UNORM\_4PACK16** = `193`

10-bit-per-channel unsigned floating-point red/green/blue/alpha channel
data with normalized value, plus 6 unused bits after each channel,
packed in 4×16 bits. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G10X6B10X6G10X6R10X6\_422\_UNORM\_4PACK16** = `194`

10-bit-per-channel unsigned floating-point green/blue/green/red channel
data with normalized value, plus 6 unused bits after each channel,
packed in 4×16 bits. Values are in the `[0.0, 1.0]` range. Blue and red
channel data is stored at halved horizontal resolution (i.e. 2
horizontally adjacent pixels will share the same value for the blue/red
channel). The green channel is listed twice, but contains different
values to allow it to be represented at full resolution.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B10X6G10X6R10X6G10X6\_422\_UNORM\_4PACK16** = `195`

10-bit-per-channel unsigned floating-point blue/green/red/green channel
data with normalized value, plus 6 unused bits after each channel,
packed in 4×16 bits. Values are in the `[0.0, 1.0]` range. Blue and red
channel data is stored at halved horizontal resolution (i.e. 2
horizontally adjacent pixels will share the same value for the blue/red
channel). The green channel is listed twice, but contains different
values to allow it to be represented at full resolution.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G10X6\_B10X6\_R10X6\_3PLANE\_420\_UNORM\_3PACK16** =
`196`

10-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 2 separate planes (green + blue + red).
Values are in the `[0.0, 1.0]` range. Blue and red channel data is
stored at halved horizontal and vertical resolution (i.e. 2×2 adjacent
pixels will share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G10X6\_B10X6R10X6\_2PLANE\_420\_UNORM\_3PACK16** = `197`

10-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 2 separate planes (green + blue/red). Values
are in the `[0.0, 1.0]` range. Blue and red channel data is stored at
halved horizontal and vertical resolution (i.e. 2×2 adjacent pixels will
share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G10X6\_B10X6\_R10X6\_3PLANE\_422\_UNORM\_3PACK16** =
`198`

10-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 3 separate planes (green + blue + red).
Values are in the `[0.0, 1.0]` range. Blue and red channel data is
stored at halved horizontal resolution (i.e. 2 horizontally adjacent
pixels will share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G10X6\_B10X6R10X6\_2PLANE\_422\_UNORM\_3PACK16** = `199`

10-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 3 separate planes (green + blue/red). Values
are in the `[0.0, 1.0]` range. Blue and red channel data is stored at
halved horizontal resolution (i.e. 2 horizontally adjacent pixels will
share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G10X6\_B10X6\_R10X6\_3PLANE\_444\_UNORM\_3PACK16** =
`200`

10-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 3 separate planes (green + blue + red).
Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R12X4\_UNORM\_PACK16** = `201`

12-bit-per-channel unsigned floating-point red channel data with
normalized value, plus 6 unused bits, packed in 16 bits. Values are in
the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R12X4G12X4\_UNORM\_2PACK16** = `202`

12-bit-per-channel unsigned floating-point red/green channel data with
normalized value, plus 6 unused bits after each channel, packed in 2×16
bits. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_R12X4G12X4B12X4A12X4\_UNORM\_4PACK16** = `203`

12-bit-per-channel unsigned floating-point red/green/blue/alpha channel
data with normalized value, plus 6 unused bits after each channel,
packed in 4×16 bits. Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G12X4B12X4G12X4R12X4\_422\_UNORM\_4PACK16** = `204`

12-bit-per-channel unsigned floating-point green/blue/green/red channel
data with normalized value, plus 6 unused bits after each channel,
packed in 4×16 bits. Values are in the `[0.0, 1.0]` range. Blue and red
channel data is stored at halved horizontal resolution (i.e. 2
horizontally adjacent pixels will share the same value for the blue/red
channel). The green channel is listed twice, but contains different
values to allow it to be represented at full resolution.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B12X4G12X4R12X4G12X4\_422\_UNORM\_4PACK16** = `205`

12-bit-per-channel unsigned floating-point blue/green/red/green channel
data with normalized value, plus 6 unused bits after each channel,
packed in 4×16 bits. Values are in the `[0.0, 1.0]` range. Blue and red
channel data is stored at halved horizontal resolution (i.e. 2
horizontally adjacent pixels will share the same value for the blue/red
channel). The green channel is listed twice, but contains different
values to allow it to be represented at full resolution.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G12X4\_B12X4\_R12X4\_3PLANE\_420\_UNORM\_3PACK16** =
`206`

12-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 2 separate planes (green + blue + red).
Values are in the `[0.0, 1.0]` range. Blue and red channel data is
stored at halved horizontal and vertical resolution (i.e. 2×2 adjacent
pixels will share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G12X4\_B12X4R12X4\_2PLANE\_420\_UNORM\_3PACK16** = `207`

12-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 2 separate planes (green + blue/red). Values
are in the `[0.0, 1.0]` range. Blue and red channel data is stored at
halved horizontal and vertical resolution (i.e. 2×2 adjacent pixels will
share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G12X4\_B12X4\_R12X4\_3PLANE\_422\_UNORM\_3PACK16** =
`208`

12-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 3 separate planes (green + blue + red).
Values are in the `[0.0, 1.0]` range. Blue and red channel data is
stored at halved horizontal resolution (i.e. 2 horizontally adjacent
pixels will share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G12X4\_B12X4R12X4\_2PLANE\_422\_UNORM\_3PACK16** = `209`

12-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 3 separate planes (green + blue/red). Values
are in the `[0.0, 1.0]` range. Blue and red channel data is stored at
halved horizontal resolution (i.e. 2 horizontally adjacent pixels will
share the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G12X4\_B12X4\_R12X4\_3PLANE\_444\_UNORM\_3PACK16** =
`210`

12-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Packed in
3×16 bits and stored across 3 separate planes (green + blue + red).
Values are in the `[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G16B16G16R16\_422\_UNORM** = `211`

16-bit-per-channel unsigned floating-point green/blue/red channel data
format with normalized value. Values are in the `[0.0, 1.0]` range. Blue
and red channel data is stored at halved horizontal resolution (i.e. 2
horizontally adjacent pixels will share the same value for the blue/red
channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_B16G16R16G16\_422\_UNORM** = `212`

16-bit-per-channel unsigned floating-point blue/green/red channel data
format with normalized value. Values are in the `[0.0, 1.0]` range. Blue
and red channel data is stored at halved horizontal resolution (i.e. 2
horizontally adjacent pixels will share the same value for the blue/red
channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G16\_B16\_R16\_3PLANE\_420\_UNORM** = `213`

16-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Stored
across 2 separate planes (green + blue + red). Values are in the
`[0.0, 1.0]` range. Blue and red channel data is stored at halved
horizontal and vertical resolution (i.e. 2×2 adjacent pixels will share
the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G16\_B16R16\_2PLANE\_420\_UNORM** = `214`

16-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Stored
across 2 separate planes (green + blue/red). Values are in the
`[0.0, 1.0]` range. Blue and red channel data is stored at halved
horizontal and vertical resolution (i.e. 2×2 adjacent pixels will share
the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G16\_B16\_R16\_3PLANE\_422\_UNORM** = `215`

16-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Stored
across 3 separate planes (green + blue + red). Values are in the
`[0.0, 1.0]` range. Blue and red channel data is stored at halved
horizontal resolution (i.e. 2 horizontally adjacent pixels will share
the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G16\_B16R16\_2PLANE\_422\_UNORM** = `216`

16-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Stored
across 3 separate planes (green + blue/red). Values are in the
`[0.0, 1.0]` range. Blue and red channel data is stored at halved
horizontal resolution (i.e. 2 horizontally adjacent pixels will share
the same value for the blue/red channel).

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>`
**DATA\_FORMAT\_G16\_B16\_R16\_3PLANE\_444\_UNORM** = `217`

16-bit-per-channel unsigned floating-point green/blue/red channel data
with normalized value, plus 6 unused bits after each channel. Stored
across 3 separate planes (green + blue + red). Values are in the
`[0.0, 1.0]` range.

classref-enumeration-constant

`DataFormat<enum_RenderingDevice_DataFormat>` **DATA\_FORMAT\_MAX** =
`218`

Represents the size of the `DataFormat<enum_RenderingDevice_DataFormat>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **BarrierMask**: `🔗<enum_RenderingDevice_BarrierMask>`

classref-enumeration-constant

`BarrierMask<enum_RenderingDevice_BarrierMask>`
**BARRIER\_MASK\_VERTEX** = `1`

Vertex shader barrier mask.

classref-enumeration-constant

`BarrierMask<enum_RenderingDevice_BarrierMask>`
**BARRIER\_MASK\_FRAGMENT** = `8`

Fragment shader barrier mask.

classref-enumeration-constant

`BarrierMask<enum_RenderingDevice_BarrierMask>`
**BARRIER\_MASK\_COMPUTE** = `2`

Compute barrier mask.

classref-enumeration-constant

`BarrierMask<enum_RenderingDevice_BarrierMask>`
**BARRIER\_MASK\_TRANSFER** = `4`

Transfer barrier mask.

classref-enumeration-constant

`BarrierMask<enum_RenderingDevice_BarrierMask>`
**BARRIER\_MASK\_RASTER** = `9`

Raster barrier mask (vertex and fragment). Equivalent to
`BARRIER_MASK_VERTEX | BARRIER_MASK_FRAGMENT`.

classref-enumeration-constant

`BarrierMask<enum_RenderingDevice_BarrierMask>`
**BARRIER\_MASK\_ALL\_BARRIERS** = `32767`

Barrier mask for all types (vertex, fragment, compute, transfer).

classref-enumeration-constant

`BarrierMask<enum_RenderingDevice_BarrierMask>`
**BARRIER\_MASK\_NO\_BARRIER** = `32768`

No barrier for any type.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureType**: `🔗<enum_RenderingDevice_TextureType>`

classref-enumeration-constant

`TextureType<enum_RenderingDevice_TextureType>` **TEXTURE\_TYPE\_1D** =
`0`

1-dimensional texture.

classref-enumeration-constant

`TextureType<enum_RenderingDevice_TextureType>` **TEXTURE\_TYPE\_2D** =
`1`

2-dimensional texture.

classref-enumeration-constant

`TextureType<enum_RenderingDevice_TextureType>` **TEXTURE\_TYPE\_3D** =
`2`

3-dimensional texture.

classref-enumeration-constant

`TextureType<enum_RenderingDevice_TextureType>` **TEXTURE\_TYPE\_CUBE**
= `3`

`Cubemap<class_Cubemap>` texture.

classref-enumeration-constant

`TextureType<enum_RenderingDevice_TextureType>`
**TEXTURE\_TYPE\_1D\_ARRAY** = `4`

Array of 1-dimensional textures.

classref-enumeration-constant

`TextureType<enum_RenderingDevice_TextureType>`
**TEXTURE\_TYPE\_2D\_ARRAY** = `5`

Array of 2-dimensional textures.

classref-enumeration-constant

`TextureType<enum_RenderingDevice_TextureType>`
**TEXTURE\_TYPE\_CUBE\_ARRAY** = `6`

Array of `Cubemap<class_Cubemap>` textures.

classref-enumeration-constant

`TextureType<enum_RenderingDevice_TextureType>` **TEXTURE\_TYPE\_MAX** =
`7`

Represents the size of the
`TextureType<enum_RenderingDevice_TextureType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureSamples**: `🔗<enum_RenderingDevice_TextureSamples>`

classref-enumeration-constant

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**TEXTURE\_SAMPLES\_1** = `0`

Perform 1 texture sample (this is the fastest but lowest-quality for
antialiasing).

classref-enumeration-constant

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**TEXTURE\_SAMPLES\_2** = `1`

Perform 2 texture samples.

classref-enumeration-constant

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**TEXTURE\_SAMPLES\_4** = `2`

Perform 4 texture samples.

classref-enumeration-constant

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**TEXTURE\_SAMPLES\_8** = `3`

Perform 8 texture samples. Not supported on mobile GPUs (including Apple
Silicon).

classref-enumeration-constant

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**TEXTURE\_SAMPLES\_16** = `4`

Perform 16 texture samples. Not supported on mobile GPUs and many
desktop GPUs.

classref-enumeration-constant

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**TEXTURE\_SAMPLES\_32** = `5`

Perform 32 texture samples. Not supported on most GPUs.

classref-enumeration-constant

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**TEXTURE\_SAMPLES\_64** = `6`

Perform 64 texture samples (this is the slowest but highest-quality for
antialiasing). Not supported on most GPUs.

classref-enumeration-constant

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**TEXTURE\_SAMPLES\_MAX** = `7`

Represents the size of the
`TextureSamples<enum_RenderingDevice_TextureSamples>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **TextureUsageBits**: `🔗<enum_RenderingDevice_TextureUsageBits>`

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_SAMPLING\_BIT** = `1`

Texture can be sampled.

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_COLOR\_ATTACHMENT\_BIT** = `2`

Texture can be used as a color attachment in a framebuffer.

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_DEPTH\_STENCIL\_ATTACHMENT\_BIT** = `4`

Texture can be used as a depth/stencil attachment in a framebuffer.

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_STORAGE\_BIT** = `8`

Texture can be used as a [storage
image](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#descriptorsets-storageimage).

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_STORAGE\_ATOMIC\_BIT** = `16`

Texture can be used as a [storage
image](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#descriptorsets-storageimage)
with support for atomic operations.

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_CPU\_READ\_BIT** = `32`

Texture can be read back on the CPU using
`texture_get_data<class_RenderingDevice_method_texture_get_data>` faster
than without this bit, since it is always kept in the system memory.

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_CAN\_UPDATE\_BIT** = `64`

Texture can be updated using
`texture_update<class_RenderingDevice_method_texture_update>`.

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_CAN\_COPY\_FROM\_BIT** = `128`

Texture can be a source for
`texture_copy<class_RenderingDevice_method_texture_copy>`.

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_CAN\_COPY\_TO\_BIT** = `256`

Texture can be a destination for
`texture_copy<class_RenderingDevice_method_texture_copy>`.

classref-enumeration-constant

`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`
**TEXTURE\_USAGE\_INPUT\_ATTACHMENT\_BIT** = `512`

Texture can be used as a [input
attachment](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#descriptorsets-inputattachment)
in a framebuffer.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureSwizzle**: `🔗<enum_RenderingDevice_TextureSwizzle>`

classref-enumeration-constant

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
**TEXTURE\_SWIZZLE\_IDENTITY** = `0`

Return the sampled value as-is.

classref-enumeration-constant

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
**TEXTURE\_SWIZZLE\_ZERO** = `1`

Always return `0.0` when sampling.

classref-enumeration-constant

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
**TEXTURE\_SWIZZLE\_ONE** = `2`

Always return `1.0` when sampling.

classref-enumeration-constant

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
**TEXTURE\_SWIZZLE\_R** = `3`

Sample the red color channel.

classref-enumeration-constant

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
**TEXTURE\_SWIZZLE\_G** = `4`

Sample the green color channel.

classref-enumeration-constant

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
**TEXTURE\_SWIZZLE\_B** = `5`

Sample the blue color channel.

classref-enumeration-constant

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
**TEXTURE\_SWIZZLE\_A** = `6`

Sample the alpha channel.

classref-enumeration-constant

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
**TEXTURE\_SWIZZLE\_MAX** = `7`

Represents the size of the
`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureSliceType**: `🔗<enum_RenderingDevice_TextureSliceType>`

classref-enumeration-constant

`TextureSliceType<enum_RenderingDevice_TextureSliceType>`
**TEXTURE\_SLICE\_2D** = `0`

2-dimensional texture slice.

classref-enumeration-constant

`TextureSliceType<enum_RenderingDevice_TextureSliceType>`
**TEXTURE\_SLICE\_CUBEMAP** = `1`

Cubemap texture slice.

classref-enumeration-constant

`TextureSliceType<enum_RenderingDevice_TextureSliceType>`
**TEXTURE\_SLICE\_3D** = `2`

3-dimensional texture slice.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SamplerFilter**: `🔗<enum_RenderingDevice_SamplerFilter>`

classref-enumeration-constant

`SamplerFilter<enum_RenderingDevice_SamplerFilter>`
**SAMPLER\_FILTER\_NEAREST** = `0`

Nearest-neighbor sampler filtering. Sampling at higher resolutions than
the source will result in a pixelated look.

classref-enumeration-constant

`SamplerFilter<enum_RenderingDevice_SamplerFilter>`
**SAMPLER\_FILTER\_LINEAR** = `1`

Bilinear sampler filtering. Sampling at higher resolutions than the
source will result in a blurry look.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SamplerRepeatMode**: `🔗<enum_RenderingDevice_SamplerRepeatMode>`

classref-enumeration-constant

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**SAMPLER\_REPEAT\_MODE\_REPEAT** = `0`

Sample with repeating enabled.

classref-enumeration-constant

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**SAMPLER\_REPEAT\_MODE\_MIRRORED\_REPEAT** = `1`

Sample with mirrored repeating enabled. When sampling outside the
`[0.0, 1.0]` range, return a mirrored version of the sampler. This
mirrored version is mirrored again if sampling further away, with the
pattern repeating indefinitely.

classref-enumeration-constant

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**SAMPLER\_REPEAT\_MODE\_CLAMP\_TO\_EDGE** = `2`

Sample with repeating disabled. When sampling outside the `[0.0, 1.0]`
range, return the color of the last pixel on the edge.

classref-enumeration-constant

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**SAMPLER\_REPEAT\_MODE\_CLAMP\_TO\_BORDER** = `3`

Sample with repeating disabled. When sampling outside the `[0.0, 1.0]`
range, return the specified
`RDSamplerState.border_color<class_RDSamplerState_property_border_color>`.

classref-enumeration-constant

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**SAMPLER\_REPEAT\_MODE\_MIRROR\_CLAMP\_TO\_EDGE** = `4`

Sample with mirrored repeating enabled, but only once. When sampling in
the `[-1.0, 0.0]` range, return a mirrored version of the sampler. When
sampling outside the `[-1.0, 1.0]` range, return the color of the last
pixel on the edge.

classref-enumeration-constant

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**SAMPLER\_REPEAT\_MODE\_MAX** = `5`

Represents the size of the
`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SamplerBorderColor**:
`🔗<enum_RenderingDevice_SamplerBorderColor>`

classref-enumeration-constant

`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
**SAMPLER\_BORDER\_COLOR\_FLOAT\_TRANSPARENT\_BLACK** = `0`

Return a floating-point transparent black color when sampling outside
the `[0.0, 1.0]` range. Only effective if the sampler repeat mode is
`SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER<class_RenderingDevice_constant_SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER>`.

classref-enumeration-constant

`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
**SAMPLER\_BORDER\_COLOR\_INT\_TRANSPARENT\_BLACK** = `1`

Return a integer transparent black color when sampling outside the
`[0.0, 1.0]` range. Only effective if the sampler repeat mode is
`SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER<class_RenderingDevice_constant_SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER>`.

classref-enumeration-constant

`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
**SAMPLER\_BORDER\_COLOR\_FLOAT\_OPAQUE\_BLACK** = `2`

Return a floating-point opaque black color when sampling outside the
`[0.0, 1.0]` range. Only effective if the sampler repeat mode is
`SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER<class_RenderingDevice_constant_SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER>`.

classref-enumeration-constant

`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
**SAMPLER\_BORDER\_COLOR\_INT\_OPAQUE\_BLACK** = `3`

Return a integer opaque black color when sampling outside the
`[0.0, 1.0]` range. Only effective if the sampler repeat mode is
`SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER<class_RenderingDevice_constant_SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER>`.

classref-enumeration-constant

`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
**SAMPLER\_BORDER\_COLOR\_FLOAT\_OPAQUE\_WHITE** = `4`

Return a floating-point opaque white color when sampling outside the
`[0.0, 1.0]` range. Only effective if the sampler repeat mode is
`SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER<class_RenderingDevice_constant_SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER>`.

classref-enumeration-constant

`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
**SAMPLER\_BORDER\_COLOR\_INT\_OPAQUE\_WHITE** = `5`

Return a integer opaque white color when sampling outside the
`[0.0, 1.0]` range. Only effective if the sampler repeat mode is
`SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER<class_RenderingDevice_constant_SAMPLER_REPEAT_MODE_CLAMP_TO_BORDER>`.

classref-enumeration-constant

`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
**SAMPLER\_BORDER\_COLOR\_MAX** = `6`

Represents the size of the
`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VertexFrequency**: `🔗<enum_RenderingDevice_VertexFrequency>`

classref-enumeration-constant

`VertexFrequency<enum_RenderingDevice_VertexFrequency>`
**VERTEX\_FREQUENCY\_VERTEX** = `0`

Vertex attribute addressing is a function of the vertex. This is used to
specify the rate at which vertex attributes are pulled from buffers.

classref-enumeration-constant

`VertexFrequency<enum_RenderingDevice_VertexFrequency>`
**VERTEX\_FREQUENCY\_INSTANCE** = `1`

Vertex attribute addressing is a function of the instance index. This is
used to specify the rate at which vertex attributes are pulled from
buffers.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **IndexBufferFormat**: `🔗<enum_RenderingDevice_IndexBufferFormat>`

classref-enumeration-constant

`IndexBufferFormat<enum_RenderingDevice_IndexBufferFormat>`
**INDEX\_BUFFER\_FORMAT\_UINT16** = `0`

Index buffer in 16-bit unsigned integer format. This limits the maximum
index that can be specified to `65535`.

classref-enumeration-constant

`IndexBufferFormat<enum_RenderingDevice_IndexBufferFormat>`
**INDEX\_BUFFER\_FORMAT\_UINT32** = `1`

Index buffer in 32-bit unsigned integer format. This limits the maximum
index that can be specified to `4294967295`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **StorageBufferUsage**:
`🔗<enum_RenderingDevice_StorageBufferUsage>`

classref-enumeration-constant

`StorageBufferUsage<enum_RenderingDevice_StorageBufferUsage>`
**STORAGE\_BUFFER\_USAGE\_DISPATCH\_INDIRECT** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **UniformType**: `🔗<enum_RenderingDevice_UniformType>`

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_SAMPLER** = `0`

Sampler uniform.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_SAMPLER\_WITH\_TEXTURE** = `1`

Sampler uniform with a texture.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_TEXTURE** = `2`

Texture uniform.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>` **UNIFORM\_TYPE\_IMAGE**
= `3`

Image uniform.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_TEXTURE\_BUFFER** = `4`

Texture buffer uniform.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_SAMPLER\_WITH\_TEXTURE\_BUFFER** = `5`

Sampler uniform with a texture buffer.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_IMAGE\_BUFFER** = `6`

Image buffer uniform.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_UNIFORM\_BUFFER** = `7`

Uniform buffer uniform.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_STORAGE\_BUFFER** = `8`

[Storage buffer](https://vkguide.dev/docs/chapter-4/storage_buffers/)
uniform.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>`
**UNIFORM\_TYPE\_INPUT\_ATTACHMENT** = `9`

Input attachment uniform.

classref-enumeration-constant

`UniformType<enum_RenderingDevice_UniformType>` **UNIFORM\_TYPE\_MAX** =
`10`

Represents the size of the
`UniformType<enum_RenderingDevice_UniformType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **RenderPrimitive**: `🔗<enum_RenderingDevice_RenderPrimitive>`

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_POINTS** = `0`

Point rendering primitive (with constant size, regardless of distance
from camera).

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_LINES** = `1`

Line list rendering primitive. Lines are drawn separated from each
other.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_LINES\_WITH\_ADJACENCY** = `2`

[Line list rendering primitive with
adjacency.](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#drawing-line-lists-with-adjacency)

\*\*Note:\*\* Adjacency is only useful with geometry shaders, which
Godot does not expose.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_LINESTRIPS** = `3`

Line strip rendering primitive. Lines drawn are connected to the
previous vertex.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_LINESTRIPS\_WITH\_ADJACENCY** = `4`

[Line strip rendering primitive with
adjacency.](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#drawing-line-strips-with-adjacency)

\*\*Note:\*\* Adjacency is only useful with geometry shaders, which
Godot does not expose.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_TRIANGLES** = `5`

Triangle list rendering primitive. Triangles are drawn separated from
each other.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_TRIANGLES\_WITH\_ADJACENCY** = `6`

[Triangle list rendering primitive with
adjacency.](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#drawing-triangle-lists-with-adjacency)

> **Note:** Adjacency is only useful with geometry shaders, which Godot
> does not expose.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_TRIANGLE\_STRIPS** = `7`

Triangle strip rendering primitive. Triangles drawn are connected to the
previous triangle.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_TRIANGLE\_STRIPS\_WITH\_AJACENCY** = `8`

[Triangle strip rendering primitive with
adjacency.](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#drawing-triangle-strips-with-adjacency)

\*\*Note:\*\* Adjacency is only useful with geometry shaders, which
Godot does not expose.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_TRIANGLE\_STRIPS\_WITH\_RESTART\_INDEX** = `9`

Triangle strip rendering primitive with *primitive restart* enabled.
Triangles drawn are connected to the previous triangle, but a primitive
restart index can be specified before drawing to create a second
triangle strip after the specified index.

\*\*Note:\*\* Only compatible with indexed draws.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_TESSELATION\_PATCH** = `10`

Tessellation patch rendering primitive. Only useful with tessellation
shaders, which can be used to deform these patches.

classref-enumeration-constant

`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`
**RENDER\_PRIMITIVE\_MAX** = `11`

Represents the size of the
`RenderPrimitive<enum_RenderingDevice_RenderPrimitive>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PolygonCullMode**: `🔗<enum_RenderingDevice_PolygonCullMode>`

classref-enumeration-constant

`PolygonCullMode<enum_RenderingDevice_PolygonCullMode>`
**POLYGON\_CULL\_DISABLED** = `0`

Do not use polygon front face or backface culling.

classref-enumeration-constant

`PolygonCullMode<enum_RenderingDevice_PolygonCullMode>`
**POLYGON\_CULL\_FRONT** = `1`

Use polygon frontface culling (faces pointing towards the camera are
hidden).

classref-enumeration-constant

`PolygonCullMode<enum_RenderingDevice_PolygonCullMode>`
**POLYGON\_CULL\_BACK** = `2`

Use polygon backface culling (faces pointing away from the camera are
hidden).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PolygonFrontFace**: `🔗<enum_RenderingDevice_PolygonFrontFace>`

classref-enumeration-constant

`PolygonFrontFace<enum_RenderingDevice_PolygonFrontFace>`
**POLYGON\_FRONT\_FACE\_CLOCKWISE** = `0`

Clockwise winding order to determine which face of a polygon is its
front face.

classref-enumeration-constant

`PolygonFrontFace<enum_RenderingDevice_PolygonFrontFace>`
**POLYGON\_FRONT\_FACE\_COUNTER\_CLOCKWISE** = `1`

Counter-clockwise winding order to determine which face of a polygon is
its front face.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **StencilOperation**: `🔗<enum_RenderingDevice_StencilOperation>`

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_KEEP** = `0`

Keep the current stencil value.

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_ZERO** = `1`

Set the stencil value to `0`.

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_REPLACE** = `2`

Replace the existing stencil value with the new one.

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_INCREMENT\_AND\_CLAMP** = `3`

Increment the existing stencil value and clamp to the maximum
representable unsigned value if reached. Stencil bits are considered as
an unsigned integer.

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_DECREMENT\_AND\_CLAMP** = `4`

Decrement the existing stencil value and clamp to the minimum value if
reached. Stencil bits are considered as an unsigned integer.

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_INVERT** = `5`

Bitwise-invert the existing stencil value.

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_INCREMENT\_AND\_WRAP** = `6`

Increment the stencil value and wrap around to `0` if reaching the
maximum representable unsigned. Stencil bits are considered as an
unsigned integer.

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_DECREMENT\_AND\_WRAP** = `7`

Decrement the stencil value and wrap around to the maximum representable
unsigned if reaching the minimum. Stencil bits are considered as an
unsigned integer.

classref-enumeration-constant

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**STENCIL\_OP\_MAX** = `8`

Represents the size of the
`StencilOperation<enum_RenderingDevice_StencilOperation>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CompareOperator**: `🔗<enum_RenderingDevice_CompareOperator>`

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_NEVER** = `0`

"Never" comparison (opposite of
`COMPARE_OP_ALWAYS<class_RenderingDevice_constant_COMPARE_OP_ALWAYS>`).

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_LESS** = `1`

"Less than" comparison.

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_EQUAL** = `2`

"Equal" comparison.

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_LESS\_OR\_EQUAL** = `3`

"Less than or equal" comparison.

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_GREATER** = `4`

"Greater than" comparison.

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_NOT\_EQUAL** = `5`

"Not equal" comparison.

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_GREATER\_OR\_EQUAL** = `6`

"Greater than or equal" comparison.

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_ALWAYS** = `7`

"Always" comparison (opposite of
`COMPARE_OP_NEVER<class_RenderingDevice_constant_COMPARE_OP_NEVER>`).

classref-enumeration-constant

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**COMPARE\_OP\_MAX** = `8`

Represents the size of the
`CompareOperator<enum_RenderingDevice_CompareOperator>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LogicOperation**: `🔗<enum_RenderingDevice_LogicOperation>`

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_CLEAR** = `0`

Clear logic operation (result is always `0`). See also
`LOGIC_OP_SET<class_RenderingDevice_constant_LOGIC_OP_SET>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>` **LOGIC\_OP\_AND**
= `1`

AND logic operation.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_AND\_REVERSE** = `2`

AND logic operation with the *destination* operand being inverted. See
also
`LOGIC_OP_AND_INVERTED<class_RenderingDevice_constant_LOGIC_OP_AND_INVERTED>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_COPY** = `3`

Copy logic operation (keeps the *source* value as-is). See also
`LOGIC_OP_COPY_INVERTED<class_RenderingDevice_constant_LOGIC_OP_COPY_INVERTED>`
and `LOGIC_OP_NO_OP<class_RenderingDevice_constant_LOGIC_OP_NO_OP>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_AND\_INVERTED** = `4`

AND logic operation with the *source* operand being inverted. See also
`LOGIC_OP_AND_REVERSE<class_RenderingDevice_constant_LOGIC_OP_AND_REVERSE>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_NO\_OP** = `5`

No-op logic operation (keeps the *destination* value as-is). See also
`LOGIC_OP_COPY<class_RenderingDevice_constant_LOGIC_OP_COPY>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>` **LOGIC\_OP\_XOR**
= `6`

Exclusive or (XOR) logic operation.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>` **LOGIC\_OP\_OR**
= `7`

OR logic operation.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>` **LOGIC\_OP\_NOR**
= `8`

Not-OR (NOR) logic operation.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_EQUIVALENT** = `9`

Not-XOR (XNOR) logic operation.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_INVERT** = `10`

Invert logic operation.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_OR\_REVERSE** = `11`

OR logic operation with the *destination* operand being inverted. See
also
`LOGIC_OP_OR_REVERSE<class_RenderingDevice_constant_LOGIC_OP_OR_REVERSE>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_COPY\_INVERTED** = `12`

NOT logic operation (inverts the value). See also
`LOGIC_OP_COPY<class_RenderingDevice_constant_LOGIC_OP_COPY>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_OR\_INVERTED** = `13`

OR logic operation with the *source* operand being inverted. See also
`LOGIC_OP_OR_REVERSE<class_RenderingDevice_constant_LOGIC_OP_OR_REVERSE>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>`
**LOGIC\_OP\_NAND** = `14`

Not-AND (NAND) logic operation.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>` **LOGIC\_OP\_SET**
= `15`

SET logic operation (result is always `1`). See also
`LOGIC_OP_CLEAR<class_RenderingDevice_constant_LOGIC_OP_CLEAR>`.

classref-enumeration-constant

`LogicOperation<enum_RenderingDevice_LogicOperation>` **LOGIC\_OP\_MAX**
= `16`

Represents the size of the
`LogicOperation<enum_RenderingDevice_LogicOperation>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BlendFactor**: `🔗<enum_RenderingDevice_BlendFactor>`

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>` **BLEND\_FACTOR\_ZERO**
= `0`

Constant `0.0` blend factor.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>` **BLEND\_FACTOR\_ONE** =
`1`

Constant `1.0` blend factor.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_SRC\_COLOR** = `2`

Color blend factor is `source color`. Alpha blend factor is
`source alpha`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_ONE\_MINUS\_SRC\_COLOR** = `3`

Color blend factor is `1.0 - source color`. Alpha blend factor is
`1.0 - source alpha`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_DST\_COLOR** = `4`

Color blend factor is `destination color`. Alpha blend factor is
`destination alpha`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_ONE\_MINUS\_DST\_COLOR** = `5`

Color blend factor is `1.0 - destination color`. Alpha blend factor is
`1.0 - destination alpha`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_SRC\_ALPHA** = `6`

Color and alpha blend factor is `source alpha`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_ONE\_MINUS\_SRC\_ALPHA** = `7`

Color and alpha blend factor is `1.0 - source alpha`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_DST\_ALPHA** = `8`

Color and alpha blend factor is `destination alpha`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_ONE\_MINUS\_DST\_ALPHA** = `9`

Color and alpha blend factor is `1.0 - destination alpha`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_CONSTANT\_COLOR** = `10`

Color blend factor is `blend constant color`. Alpha blend factor is
`blend constant alpha` (see
`draw_list_set_blend_constants<class_RenderingDevice_method_draw_list_set_blend_constants>`).

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_ONE\_MINUS\_CONSTANT\_COLOR** = `11`

Color blend factor is `1.0 - blend constant color`. Alpha blend factor
is `1.0 - blend constant alpha` (see
`draw_list_set_blend_constants<class_RenderingDevice_method_draw_list_set_blend_constants>`).

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_CONSTANT\_ALPHA** = `12`

Color and alpha blend factor is `blend constant alpha` (see
`draw_list_set_blend_constants<class_RenderingDevice_method_draw_list_set_blend_constants>`).

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_ONE\_MINUS\_CONSTANT\_ALPHA** = `13`

Color and alpha blend factor is `1.0 - blend constant alpha` (see
`draw_list_set_blend_constants<class_RenderingDevice_method_draw_list_set_blend_constants>`).

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_SRC\_ALPHA\_SATURATE** = `14`

Color blend factor is `min(source alpha, 1.0 - destination alpha)`.
Alpha blend factor is `1.0`.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_SRC1\_COLOR** = `15`

Color blend factor is `second source color`. Alpha blend factor is
`second source alpha`. Only relevant for dual-source blending.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_ONE\_MINUS\_SRC1\_COLOR** = `16`

Color blend factor is `1.0 - second source color`. Alpha blend factor is
`1.0 - second source alpha`. Only relevant for dual-source blending.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_SRC1\_ALPHA** = `17`

Color and alpha blend factor is `second source alpha`. Only relevant for
dual-source blending.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>`
**BLEND\_FACTOR\_ONE\_MINUS\_SRC1\_ALPHA** = `18`

Color and alpha blend factor is `1.0 - second source alpha`. Only
relevant for dual-source blending.

classref-enumeration-constant

`BlendFactor<enum_RenderingDevice_BlendFactor>` **BLEND\_FACTOR\_MAX** =
`19`

Represents the size of the
`BlendFactor<enum_RenderingDevice_BlendFactor>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BlendOperation**: `🔗<enum_RenderingDevice_BlendOperation>`

classref-enumeration-constant

`BlendOperation<enum_RenderingDevice_BlendOperation>` **BLEND\_OP\_ADD**
= `0`

Additive blending operation (`source + destination`).

classref-enumeration-constant

`BlendOperation<enum_RenderingDevice_BlendOperation>`
**BLEND\_OP\_SUBTRACT** = `1`

Subtractive blending operation (`source - destination`).

classref-enumeration-constant

`BlendOperation<enum_RenderingDevice_BlendOperation>`
**BLEND\_OP\_REVERSE\_SUBTRACT** = `2`

Reverse subtractive blending operation (`destination - source`).

classref-enumeration-constant

`BlendOperation<enum_RenderingDevice_BlendOperation>`
**BLEND\_OP\_MINIMUM** = `3`

Minimum blending operation (keep the lowest value of the two).

classref-enumeration-constant

`BlendOperation<enum_RenderingDevice_BlendOperation>`
**BLEND\_OP\_MAXIMUM** = `4`

Maximum blending operation (keep the highest value of the two).

classref-enumeration-constant

`BlendOperation<enum_RenderingDevice_BlendOperation>` **BLEND\_OP\_MAX**
= `5`

Represents the size of the
`BlendOperation<enum_RenderingDevice_BlendOperation>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **PipelineDynamicStateFlags**:
`🔗<enum_RenderingDevice_PipelineDynamicStateFlags>`

classref-enumeration-constant

`PipelineDynamicStateFlags<enum_RenderingDevice_PipelineDynamicStateFlags>`
**DYNAMIC\_STATE\_LINE\_WIDTH** = `1`

Allows dynamically changing the width of rendering lines.

classref-enumeration-constant

`PipelineDynamicStateFlags<enum_RenderingDevice_PipelineDynamicStateFlags>`
**DYNAMIC\_STATE\_DEPTH\_BIAS** = `2`

Allows dynamically changing the depth bias.

classref-enumeration-constant

`PipelineDynamicStateFlags<enum_RenderingDevice_PipelineDynamicStateFlags>`
**DYNAMIC\_STATE\_BLEND\_CONSTANTS** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`PipelineDynamicStateFlags<enum_RenderingDevice_PipelineDynamicStateFlags>`
**DYNAMIC\_STATE\_DEPTH\_BOUNDS** = `8`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`PipelineDynamicStateFlags<enum_RenderingDevice_PipelineDynamicStateFlags>`
**DYNAMIC\_STATE\_STENCIL\_COMPARE\_MASK** = `16`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`PipelineDynamicStateFlags<enum_RenderingDevice_PipelineDynamicStateFlags>`
**DYNAMIC\_STATE\_STENCIL\_WRITE\_MASK** = `32`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`PipelineDynamicStateFlags<enum_RenderingDevice_PipelineDynamicStateFlags>`
**DYNAMIC\_STATE\_STENCIL\_REFERENCE** = `64`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **InitialAction**: `🔗<enum_RenderingDevice_InitialAction>`

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_LOAD** = `0`

Load the previous contents of the framebuffer.

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_CLEAR** = `1`

Clear the whole framebuffer or its specified region.

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_DISCARD** = `2`

Ignore the previous contents of the framebuffer. This is the fastest
option if you'll overwrite all of the pixels and don't need to read any
of them.

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_MAX** = `3`

Represents the size of the
`InitialAction<enum_RenderingDevice_InitialAction>` enum.

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_CLEAR\_REGION** = `1`

**Deprecated:** Use
`INITIAL_ACTION_CLEAR<class_RenderingDevice_constant_INITIAL_ACTION_CLEAR>`
instead.

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_CLEAR\_REGION\_CONTINUE** = `1`

**Deprecated:** Use
`INITIAL_ACTION_LOAD<class_RenderingDevice_constant_INITIAL_ACTION_LOAD>`
instead.

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_KEEP** = `0`

**Deprecated:** Use
`INITIAL_ACTION_LOAD<class_RenderingDevice_constant_INITIAL_ACTION_LOAD>`
instead.

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_DROP** = `2`

**Deprecated:** Use
`INITIAL_ACTION_DISCARD<class_RenderingDevice_constant_INITIAL_ACTION_DISCARD>`
instead.

classref-enumeration-constant

`InitialAction<enum_RenderingDevice_InitialAction>`
**INITIAL\_ACTION\_CONTINUE** = `0`

**Deprecated:** Use
`INITIAL_ACTION_LOAD<class_RenderingDevice_constant_INITIAL_ACTION_LOAD>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FinalAction**: `🔗<enum_RenderingDevice_FinalAction>`

classref-enumeration-constant

`FinalAction<enum_RenderingDevice_FinalAction>` **FINAL\_ACTION\_STORE**
= `0`

Store the result of the draw list in the framebuffer. This is generally
what you want to do.

classref-enumeration-constant

`FinalAction<enum_RenderingDevice_FinalAction>`
**FINAL\_ACTION\_DISCARD** = `1`

Discard the contents of the framebuffer. This is the fastest option if
you don't need to use the results of the draw list.

classref-enumeration-constant

`FinalAction<enum_RenderingDevice_FinalAction>` **FINAL\_ACTION\_MAX** =
`2`

Represents the size of the
`FinalAction<enum_RenderingDevice_FinalAction>` enum.

classref-enumeration-constant

`FinalAction<enum_RenderingDevice_FinalAction>` **FINAL\_ACTION\_READ**
= `0`

**Deprecated:** Use
`FINAL_ACTION_STORE<class_RenderingDevice_constant_FINAL_ACTION_STORE>`
instead.

classref-enumeration-constant

`FinalAction<enum_RenderingDevice_FinalAction>`
**FINAL\_ACTION\_CONTINUE** = `0`

**Deprecated:** Use
`FINAL_ACTION_STORE<class_RenderingDevice_constant_FINAL_ACTION_STORE>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ShaderStage**: `🔗<enum_RenderingDevice_ShaderStage>`

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_VERTEX** = `0`

Vertex shader stage. This can be used to manipulate vertices from a
shader (but not create new vertices).

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_FRAGMENT** = `1`

Fragment shader stage (called "pixel shader" in Direct3D). This can be
used to manipulate pixels from a shader.

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_TESSELATION\_CONTROL** = `2`

Tessellation control shader stage. This can be used to create additional
geometry from a shader.

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_TESSELATION\_EVALUATION** = `3`

Tessellation evaluation shader stage. This can be used to create
additional geometry from a shader.

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_COMPUTE** = `4`

Compute shader stage. This can be used to run arbitrary computing tasks
in a shader, performing them on the GPU instead of the CPU.

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>` **SHADER\_STAGE\_MAX** =
`5`

Represents the size of the
`ShaderStage<enum_RenderingDevice_ShaderStage>` enum.

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_VERTEX\_BIT** = `1`

Vertex shader stage bit (see also
`SHADER_STAGE_VERTEX<class_RenderingDevice_constant_SHADER_STAGE_VERTEX>`).

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_FRAGMENT\_BIT** = `2`

Fragment shader stage bit (see also
`SHADER_STAGE_FRAGMENT<class_RenderingDevice_constant_SHADER_STAGE_FRAGMENT>`).

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_TESSELATION\_CONTROL\_BIT** = `4`

Tessellation control shader stage bit (see also
`SHADER_STAGE_TESSELATION_CONTROL<class_RenderingDevice_constant_SHADER_STAGE_TESSELATION_CONTROL>`).

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_TESSELATION\_EVALUATION\_BIT** = `8`

Tessellation evaluation shader stage bit (see also
`SHADER_STAGE_TESSELATION_EVALUATION<class_RenderingDevice_constant_SHADER_STAGE_TESSELATION_EVALUATION>`).

classref-enumeration-constant

`ShaderStage<enum_RenderingDevice_ShaderStage>`
**SHADER\_STAGE\_COMPUTE\_BIT** = `16`

Compute shader stage bit (see also
`SHADER_STAGE_COMPUTE<class_RenderingDevice_constant_SHADER_STAGE_COMPUTE>`).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ShaderLanguage**: `🔗<enum_RenderingDevice_ShaderLanguage>`

classref-enumeration-constant

`ShaderLanguage<enum_RenderingDevice_ShaderLanguage>`
**SHADER\_LANGUAGE\_GLSL** = `0`

Khronos' GLSL shading language (used natively by OpenGL and Vulkan).
This is the language used for core Godot shaders.

classref-enumeration-constant

`ShaderLanguage<enum_RenderingDevice_ShaderLanguage>`
**SHADER\_LANGUAGE\_HLSL** = `1`

Microsoft's High-Level Shading Language (used natively by Direct3D, but
can also be used in Vulkan).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PipelineSpecializationConstantType**:
`🔗<enum_RenderingDevice_PipelineSpecializationConstantType>`

classref-enumeration-constant

`PipelineSpecializationConstantType<enum_RenderingDevice_PipelineSpecializationConstantType>`
**PIPELINE\_SPECIALIZATION\_CONSTANT\_TYPE\_BOOL** = `0`

Boolean specialization constant.

classref-enumeration-constant

`PipelineSpecializationConstantType<enum_RenderingDevice_PipelineSpecializationConstantType>`
**PIPELINE\_SPECIALIZATION\_CONSTANT\_TYPE\_INT** = `1`

Integer specialization constant.

classref-enumeration-constant

`PipelineSpecializationConstantType<enum_RenderingDevice_PipelineSpecializationConstantType>`
**PIPELINE\_SPECIALIZATION\_CONSTANT\_TYPE\_FLOAT** = `2`

Floating-point specialization constant.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Limit**: `🔗<enum_RenderingDevice_Limit>`

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_BOUND\_UNIFORM\_SETS**
= `0`

Maximum number of uniform sets that can be bound at a given time.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_FRAMEBUFFER\_COLOR\_ATTACHMENTS** = `1`

Maximum number of color framebuffer attachments that can be used at a
given time.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_TEXTURES\_PER\_UNIFORM\_SET** = `2`

Maximum number of textures that can be used per uniform set.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_SAMPLERS\_PER\_UNIFORM\_SET** = `3`

Maximum number of samplers that can be used per uniform set.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_STORAGE\_BUFFERS\_PER\_UNIFORM\_SET** = `4`

Maximum number of [storage
buffers](https://vkguide.dev/docs/chapter-4/storage_buffers/) per
uniform set.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_STORAGE\_IMAGES\_PER\_UNIFORM\_SET** = `5`

Maximum number of storage images per uniform set.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_UNIFORM\_BUFFERS\_PER\_UNIFORM\_SET** = `6`

Maximum number of uniform buffers per uniform set.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_DRAW\_INDEXED\_INDEX**
= `7`

Maximum index for an indexed draw command.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_FRAMEBUFFER\_HEIGHT**
= `8`

Maximum height of a framebuffer (in pixels).

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_FRAMEBUFFER\_WIDTH** =
`9`

Maximum width of a framebuffer (in pixels).

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_TEXTURE\_ARRAY\_LAYERS** = `10`

Maximum number of texture array layers.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_TEXTURE\_SIZE\_1D** =
`11`

Maximum supported 1-dimensional texture size (in pixels on a single
axis).

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_TEXTURE\_SIZE\_2D** =
`12`

Maximum supported 2-dimensional texture size (in pixels on a single
axis).

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_TEXTURE\_SIZE\_3D** =
`13`

Maximum supported 3-dimensional texture size (in pixels on a single
axis).

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_TEXTURE\_SIZE\_CUBE**
= `14`

Maximum supported cubemap texture size (in pixels on a single axis of a
single face).

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_TEXTURES\_PER\_SHADER\_STAGE** = `15`

Maximum number of textures per shader stage.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_SAMPLERS\_PER\_SHADER\_STAGE** = `16`

Maximum number of samplers per shader stage.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_STORAGE\_BUFFERS\_PER\_SHADER\_STAGE** = `17`

Maximum number of [storage
buffers](https://vkguide.dev/docs/chapter-4/storage_buffers/) per shader
stage.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_STORAGE\_IMAGES\_PER\_SHADER\_STAGE** = `18`

Maximum number of storage images per shader stage.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_UNIFORM\_BUFFERS\_PER\_SHADER\_STAGE** = `19`

Maximum number of uniform buffers per uniform set.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>` **LIMIT\_MAX\_PUSH\_CONSTANT\_SIZE**
= `20`

Maximum size of a push constant. A lot of devices are limited to 128
bytes, so try to avoid exceeding 128 bytes in push constants to ensure
compatibility even if your GPU is reporting a higher value.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_UNIFORM\_BUFFER\_SIZE** = `21`

Maximum size of a uniform buffer.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_VERTEX\_INPUT\_ATTRIBUTE\_OFFSET** = `22`

Maximum vertex input attribute offset.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_VERTEX\_INPUT\_ATTRIBUTES** = `23`

Maximum number of vertex input attributes.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_VERTEX\_INPUT\_BINDINGS** = `24`

Maximum number of vertex input bindings.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_VERTEX\_INPUT\_BINDING\_STRIDE** = `25`

Maximum vertex input binding stride.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MIN\_UNIFORM\_BUFFER\_OFFSET\_ALIGNMENT** = `26`

Minimum uniform buffer offset alignment.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_COMPUTE\_SHARED\_MEMORY\_SIZE** = `27`

Maximum shared memory size for compute shaders.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_COMPUTE\_WORKGROUP\_COUNT\_X** = `28`

Maximum number of workgroups for compute shaders on the X axis.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_COMPUTE\_WORKGROUP\_COUNT\_Y** = `29`

Maximum number of workgroups for compute shaders on the Y axis.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_COMPUTE\_WORKGROUP\_COUNT\_Z** = `30`

Maximum number of workgroups for compute shaders on the Z axis.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_COMPUTE\_WORKGROUP\_INVOCATIONS** = `31`

Maximum number of workgroup invocations for compute shaders.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_COMPUTE\_WORKGROUP\_SIZE\_X** = `32`

Maximum workgroup size for compute shaders on the X axis.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_COMPUTE\_WORKGROUP\_SIZE\_Y** = `33`

Maximum workgroup size for compute shaders on the Y axis.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_COMPUTE\_WORKGROUP\_SIZE\_Z** = `34`

Maximum workgroup size for compute shaders on the Z axis.

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_VIEWPORT\_DIMENSIONS\_X** = `35`

Maximum viewport width (in pixels).

classref-enumeration-constant

`Limit<enum_RenderingDevice_Limit>`
**LIMIT\_MAX\_VIEWPORT\_DIMENSIONS\_Y** = `36`

Maximum viewport height (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MemoryType**: `🔗<enum_RenderingDevice_MemoryType>`

classref-enumeration-constant

`MemoryType<enum_RenderingDevice_MemoryType>` **MEMORY\_TEXTURES** = `0`

Memory taken by textures.

classref-enumeration-constant

`MemoryType<enum_RenderingDevice_MemoryType>` **MEMORY\_BUFFERS** = `1`

Memory taken by buffers.

classref-enumeration-constant

`MemoryType<enum_RenderingDevice_MemoryType>` **MEMORY\_TOTAL** = `2`

Total memory taken. This is greater than the sum of
`MEMORY_TEXTURES<class_RenderingDevice_constant_MEMORY_TEXTURES>` and
`MEMORY_BUFFERS<class_RenderingDevice_constant_MEMORY_BUFFERS>`, as it
also includes miscellaneous memory usage.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BreadcrumbMarker**: `🔗<enum_RenderingDevice_BreadcrumbMarker>`

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>` **NONE** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**REFLECTION\_PROBES** = `65536`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>` **SKY\_PASS**
= `131072`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**LIGHTMAPPER\_PASS** = `196608`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**SHADOW\_PASS\_DIRECTIONAL** = `262144`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**SHADOW\_PASS\_CUBE** = `327680`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**OPAQUE\_PASS** = `393216`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**ALPHA\_PASS** = `458752`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**TRANSPARENT\_PASS** = `524288`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**POST\_PROCESSING\_PASS** = `589824`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>` **BLIT\_PASS**
= `655360`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>` **UI\_PASS** =
`720896`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>`
**DEBUG\_PASS** = `786432`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**INVALID\_ID** = `-1` `🔗<class_RenderingDevice_constant_INVALID_ID>`

Returned by functions that return an ID if a value is invalid.

classref-constant

**INVALID\_FORMAT\_ID** = `-1`
`🔗<class_RenderingDevice_constant_INVALID_FORMAT_ID>`

Returned by functions that return a format ID if a value is invalid.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **barrier**(from:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`BarrierMask<enum_RenderingDevice_BarrierMask>`\]
= 32767, to:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`BarrierMask<enum_RenderingDevice_BarrierMask>`\]
= 32767) `🔗<class_RenderingDevice_method_barrier>`

**Deprecated:** Barriers are automatically inserted by RenderingDevice.

This method does nothing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **buffer\_clear**(buffer:
`RID<class_RID>`, offset: `int<class_int>`, size\_bytes:
`int<class_int>`) `🔗<class_RenderingDevice_method_buffer_clear>`

Clears the contents of the `buffer`, clearing `size_bytes` bytes,
starting at `offset`.

Prints an error if:

-   the size isn't a multiple of four
-   the region specified by `offset` + `size_bytes` exceeds the buffer
-   a draw list is currently active (created by
    `draw_list_begin<class_RenderingDevice_method_draw_list_begin>`)
-   a compute list is currently active (created by
    `compute_list_begin<class_RenderingDevice_method_compute_list_begin>`)

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **buffer\_copy**(src\_buffer:
`RID<class_RID>`, dst\_buffer: `RID<class_RID>`, src\_offset:
`int<class_int>`, dst\_offset: `int<class_int>`, size: `int<class_int>`)
`🔗<class_RenderingDevice_method_buffer_copy>`

Copies `size` bytes from the `src_buffer` at `src_offset` into
`dst_buffer` at `dst_offset`.

Prints an error if:

-   `size` exceeds the size of either `src_buffer` or `dst_buffer` at
    their corresponding offsets
-   a draw list is currently active (created by
    `draw_list_begin<class_RenderingDevice_method_draw_list_begin>`)
-   a compute list is currently active (created by
    `compute_list_begin<class_RenderingDevice_method_compute_list_begin>`)

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **buffer\_get\_data**(buffer:
`RID<class_RID>`, offset\_bytes: `int<class_int>` = 0, size\_bytes:
`int<class_int>` = 0) `🔗<class_RenderingDevice_method_buffer_get_data>`

Returns a copy of the data of the specified `buffer`, optionally
`offset_bytes` and `size_bytes` can be set to copy only a portion of the
buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **buffer\_update**(buffer:
`RID<class_RID>`, offset: `int<class_int>`, size\_bytes:
`int<class_int>`, data: `PackedByteArray<class_PackedByteArray>`)
`🔗<class_RenderingDevice_method_buffer_update>`

Updates a region of `size_bytes` bytes, starting at `offset`, in the
buffer, with the specified `data`.

Prints an error if:

-   the region specified by `offset` + `size_bytes` exceeds the buffer
-   a draw list is currently active (created by
    `draw_list_begin<class_RenderingDevice_method_draw_list_begin>`)
-   a compute list is currently active (created by
    `compute_list_begin<class_RenderingDevice_method_compute_list_begin>`)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **capture\_timestamp**(name:
`String<class_String>`)
`🔗<class_RenderingDevice_method_capture_timestamp>`

Creates a timestamp marker with the specified `name`. This is used for
performance reporting with the
`get_captured_timestamp_cpu_time<class_RenderingDevice_method_get_captured_timestamp_cpu_time>`,
`get_captured_timestamp_gpu_time<class_RenderingDevice_method_get_captured_timestamp_gpu_time>`
and
`get_captured_timestamp_name<class_RenderingDevice_method_get_captured_timestamp_name>`
methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **compute\_list\_add\_barrier**(compute\_list:
`int<class_int>`)
`🔗<class_RenderingDevice_method_compute_list_add_barrier>`

Raises a Vulkan compute barrier in the specified `compute_list`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **compute\_list\_begin**()
`🔗<class_RenderingDevice_method_compute_list_begin>`

Starts a list of compute commands created with the `compute_*` methods.
The returned value should be passed to other `compute_list_*` functions.

Multiple compute lists cannot be created at the same time; you must
finish the previous compute list first using
`compute_list_end<class_RenderingDevice_method_compute_list_end>`.

A simple compute operation might look like this (code is not a complete
example):

    var rd = RenderingDevice.new()
    var compute_list = rd.compute_list_begin()

    rd.compute_list_bind_compute_pipeline(compute_list, compute_shader_dilate_pipeline)
    rd.compute_list_bind_uniform_set(compute_list, compute_base_uniform_set, 0)
    rd.compute_list_bind_uniform_set(compute_list, dilate_uniform_set, 1)

    for i in atlas_slices:
        rd.compute_list_set_push_constant(compute_list, push_constant, push_constant.size())
        rd.compute_list_dispatch(compute_list, group_size.x, group_size.y, group_size.z)
        # No barrier, let them run all together.

    rd.compute_list_end()

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**compute\_list\_bind\_compute\_pipeline**(compute\_list:
`int<class_int>`, compute\_pipeline: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_compute_list_bind_compute_pipeline>`

Tells the GPU what compute pipeline to use when processing the compute
list. If the shader has changed since the last time this function was
called, Godot will unbind all descriptor sets and will re-bind them
inside
`compute_list_dispatch<class_RenderingDevice_method_compute_list_dispatch>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**compute\_list\_bind\_uniform\_set**(compute\_list: `int<class_int>`,
uniform\_set: `RID<class_RID>`, set\_index: `int<class_int>`)
`🔗<class_RenderingDevice_method_compute_list_bind_uniform_set>`

Binds the `uniform_set` to this `compute_list`. Godot ensures that all
textures in the uniform set have the correct Vulkan access masks. If
Godot had to change access masks of textures, it will raise a Vulkan
image memory barrier.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **compute\_list\_dispatch**(compute\_list:
`int<class_int>`, x\_groups: `int<class_int>`, y\_groups:
`int<class_int>`, z\_groups: `int<class_int>`)
`🔗<class_RenderingDevice_method_compute_list_dispatch>`

Submits the compute list for processing on the GPU. This is the compute
equivalent to
`draw_list_draw<class_RenderingDevice_method_draw_list_draw>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**compute\_list\_dispatch\_indirect**(compute\_list: `int<class_int>`,
buffer: `RID<class_RID>`, offset: `int<class_int>`)
`🔗<class_RenderingDevice_method_compute_list_dispatch_indirect>`

Submits the compute list for processing on the GPU with the given group
counts stored in the `buffer` at `offset`. Buffer must have been created
with
`STORAGE_BUFFER_USAGE_DISPATCH_INDIRECT<class_RenderingDevice_constant_STORAGE_BUFFER_USAGE_DISPATCH_INDIRECT>`
flag.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **compute\_list\_end**()
`🔗<class_RenderingDevice_method_compute_list_end>`

Finishes a list of compute commands created with the `compute_*`
methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**compute\_list\_set\_push\_constant**(compute\_list: `int<class_int>`,
buffer: `PackedByteArray<class_PackedByteArray>`, size\_bytes:
`int<class_int>`)
`🔗<class_RenderingDevice_method_compute_list_set_push_constant>`

Sets the push constant data to `buffer` for the specified
`compute_list`. The shader determines how this binary data is used. The
buffer's size in bytes must also be specified in `size_bytes` (this can
be obtained by calling the
`PackedByteArray.size<class_PackedByteArray_method_size>` method on the
passed `buffer`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **compute\_pipeline\_create**(shader: `RID<class_RID>`,
specialization\_constants:
`Array<class_Array>`\[`RDPipelineSpecializationConstant<class_RDPipelineSpecializationConstant>`\]
= \[\]) `🔗<class_RenderingDevice_method_compute_pipeline_create>`

Creates a new compute pipeline. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **compute\_pipeline\_is\_valid**(compute\_pipeline:
`RID<class_RID>`)
`🔗<class_RenderingDevice_method_compute_pipeline_is_valid>`

Returns `true` if the compute pipeline specified by the
`compute_pipeline` RID is valid, `false` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RenderingDevice<class_RenderingDevice>` **create\_local\_device**()
`🔗<class_RenderingDevice_method_create_local_device>`

Create a new local **RenderingDevice**. This is most useful for
performing compute operations on the GPU independently from the rest of
the engine.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_command\_begin\_label**(name:
`String<class_String>`, color: `Color<class_Color>`)
`🔗<class_RenderingDevice_method_draw_command_begin_label>`

Create a command buffer debug label region that can be displayed in
third-party tools such as [RenderDoc](https://renderdoc.org/). All
regions must be ended with a
`draw_command_end_label<class_RenderingDevice_method_draw_command_end_label>`
call. When viewed from the linear series of submissions to a single
queue, calls to
`draw_command_begin_label<class_RenderingDevice_method_draw_command_begin_label>`
and
`draw_command_end_label<class_RenderingDevice_method_draw_command_end_label>`
must be matched and balanced.

The `VK_EXT_DEBUG_UTILS_EXTENSION_NAME` Vulkan extension must be
available and enabled for command buffer debug label region to work. See
also
`draw_command_end_label<class_RenderingDevice_method_draw_command_end_label>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_command\_end\_label**()
`🔗<class_RenderingDevice_method_draw_command_end_label>`

Ends the command buffer debug label region started by a
`draw_command_begin_label<class_RenderingDevice_method_draw_command_begin_label>`
call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_command\_insert\_label**(name:
`String<class_String>`, color: `Color<class_Color>`)
`🔗<class_RenderingDevice_method_draw_command_insert_label>`

**Deprecated:** Inserting labels no longer applies due to command
reordering.

This method does nothing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **draw\_list\_begin**(framebuffer: `RID<class_RID>`,
initial\_color\_action:
`InitialAction<enum_RenderingDevice_InitialAction>`,
final\_color\_action: `FinalAction<enum_RenderingDevice_FinalAction>`,
initial\_depth\_action:
`InitialAction<enum_RenderingDevice_InitialAction>`,
final\_depth\_action: `FinalAction<enum_RenderingDevice_FinalAction>`,
clear\_color\_values: `PackedColorArray<class_PackedColorArray>` =
PackedColorArray(), clear\_depth: `float<class_float>` = 1.0,
clear\_stencil: `int<class_int>` = 0, region: `Rect2<class_Rect2>` =
Rect2(0, 0, 0, 0), breadcrumb: `int<class_int>` = 0)
`🔗<class_RenderingDevice_method_draw_list_begin>`

Starts a list of raster drawing commands created with the `draw_*`
methods. The returned value should be passed to other `draw_list_*`
functions.

Multiple draw lists cannot be created at the same time; you must finish
the previous draw list first using
`draw_list_end<class_RenderingDevice_method_draw_list_end>`.

A simple drawing operation might look like this (code is not a complete
example):

    var rd = RenderingDevice.new()
    var clear_colors = PackedColorArray([Color(0, 0, 0, 0), Color(0, 0, 0, 0), Color(0, 0, 0, 0)])
    var draw_list = rd.draw_list_begin(framebuffers[i], RenderingDevice.INITIAL_ACTION_CLEAR, RenderingDevice.FINAL_ACTION_READ, RenderingDevice.INITIAL_ACTION_CLEAR, RenderingDevice.FINAL_ACTION_DISCARD, clear_colors, RenderingDevice.OPAQUE_PASS)

    # Draw opaque.
    rd.draw_list_bind_render_pipeline(draw_list, raster_pipeline)
    rd.draw_list_bind_uniform_set(draw_list, raster_base_uniform, 0)
    rd.draw_list_set_push_constant(draw_list, raster_push_constant, raster_push_constant.size())
    rd.draw_list_draw(draw_list, false, 1, slice_triangle_count[i] * 3)
    # Draw wire.
    rd.draw_list_bind_render_pipeline(draw_list, raster_pipeline_wire)
    rd.draw_list_bind_uniform_set(draw_list, raster_base_uniform, 0)
    rd.draw_list_set_push_constant(draw_list, raster_push_constant, raster_push_constant.size())
    rd.draw_list_draw(draw_list, false, 1, slice_triangle_count[i] * 3)

    rd.draw_list_end()

The `breadcrumb` parameter can be an arbitrary 32-bit integer that is
useful to diagnose GPU crashes. If Godot is built in dev or debug mode;
when the GPU crashes Godot will dump all shaders that were being
executed at the time of the crash and the breadcrumb is useful to
diagnose what passes did those shaders belong to.

It does not affect rendering behavior and can be set to 0. It is
recommended to use
`BreadcrumbMarker<enum_RenderingDevice_BreadcrumbMarker>` enumerations
for consistency but it's not required. It is also possible to use
bitwise operations to add extra data. e.g.

    rd.draw_list_begin(fb[i], RenderingDevice.INITIAL_ACTION_CLEAR, RenderingDevice.FINAL_ACTION_READ, RenderingDevice.INITIAL_ACTION_CLEAR, RenderingDevice.FINAL_ACTION_DISCARD, clear_colors, RenderingDevice.OPAQUE_PASS | 5)

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **draw\_list\_begin\_for\_screen**(screen:
`int<class_int>` = 0, clear\_color: `Color<class_Color>` = Color(0, 0,
0, 1)) `🔗<class_RenderingDevice_method_draw_list_begin_for_screen>`

High-level variant of
`draw_list_begin<class_RenderingDevice_method_draw_list_begin>`, with
the parameters automatically being adjusted for drawing onto the window
specified by the `screen` ID.

\*\*Note:\*\* Cannot be used with local RenderingDevices, as these don't
have a screen. If called on a local RenderingDevice,
`draw_list_begin_for_screen<class_RenderingDevice_method_draw_list_begin_for_screen>`
returns `INVALID_ID<class_RenderingDevice_constant_INVALID_ID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>`
**draw\_list\_begin\_split**(framebuffer: `RID<class_RID>`, splits:
`int<class_int>`, initial\_color\_action:
`InitialAction<enum_RenderingDevice_InitialAction>`,
final\_color\_action: `FinalAction<enum_RenderingDevice_FinalAction>`,
initial\_depth\_action:
`InitialAction<enum_RenderingDevice_InitialAction>`,
final\_depth\_action: `FinalAction<enum_RenderingDevice_FinalAction>`,
clear\_color\_values: `PackedColorArray<class_PackedColorArray>` =
PackedColorArray(), clear\_depth: `float<class_float>` = 1.0,
clear\_stencil: `int<class_int>` = 0, region: `Rect2<class_Rect2>` =
Rect2(0, 0, 0, 0), storage\_textures:
`Array<class_Array>`\[`RID<class_RID>`\] = \[\])
`🔗<class_RenderingDevice_method_draw_list_begin_split>`

**Deprecated:** Split draw lists are used automatically by
RenderingDevice.

This method does nothing and always returns an empty
`PackedInt64Array<class_PackedInt64Array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_list\_bind\_index\_array**(draw\_list:
`int<class_int>`, index\_array: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_draw_list_bind_index_array>`

Binds `index_array` to the specified `draw_list`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**draw\_list\_bind\_render\_pipeline**(draw\_list: `int<class_int>`,
render\_pipeline: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_draw_list_bind_render_pipeline>`

Binds `render_pipeline` to the specified `draw_list`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_list\_bind\_uniform\_set**(draw\_list:
`int<class_int>`, uniform\_set: `RID<class_RID>`, set\_index:
`int<class_int>`)
`🔗<class_RenderingDevice_method_draw_list_bind_uniform_set>`

Binds `uniform_set` to the specified `draw_list`. A `set_index` must
also be specified, which is an identifier starting from `0` that must
match the one expected by the draw list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**draw\_list\_bind\_vertex\_array**(draw\_list: `int<class_int>`,
vertex\_array: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_draw_list_bind_vertex_array>`

Binds `vertex_array` to the specified `draw_list`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_list\_disable\_scissor**(draw\_list:
`int<class_int>`)
`🔗<class_RenderingDevice_method_draw_list_disable_scissor>`

Removes and disables the scissor rectangle for the specified
`draw_list`. See also
`draw_list_enable_scissor<class_RenderingDevice_method_draw_list_enable_scissor>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_list\_draw**(draw\_list:
`int<class_int>`, use\_indices: `bool<class_bool>`, instances:
`int<class_int>`, procedural\_vertex\_count: `int<class_int>` = 0)
`🔗<class_RenderingDevice_method_draw_list_draw>`

Submits `draw_list` for rendering on the GPU. This is the raster
equivalent to
`compute_list_dispatch<class_RenderingDevice_method_compute_list_dispatch>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_list\_enable\_scissor**(draw\_list:
`int<class_int>`, rect: `Rect2<class_Rect2>` = Rect2(0, 0, 0, 0))
`🔗<class_RenderingDevice_method_draw_list_enable_scissor>`

Creates a scissor rectangle and enables it for the specified
`draw_list`. Scissor rectangles are used for clipping by discarding
fragments that fall outside a specified rectangular portion of the
screen. See also
`draw_list_disable_scissor<class_RenderingDevice_method_draw_list_disable_scissor>`.

\*\*Note:\*\* The specified `rect` is automatically intersected with the
screen's dimensions, which means it cannot exceed the screen's
dimensions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_list\_end**()
`🔗<class_RenderingDevice_method_draw_list_end>`

Finishes a list of raster drawing commands created with the `draw_*`
methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**draw\_list\_set\_blend\_constants**(draw\_list: `int<class_int>`,
color: `Color<class_Color>`)
`🔗<class_RenderingDevice_method_draw_list_set_blend_constants>`

Sets blend constants for the specified `draw_list` to `color`. Blend
constants are used only if the graphics pipeline is created with
`DYNAMIC_STATE_BLEND_CONSTANTS<class_RenderingDevice_constant_DYNAMIC_STATE_BLEND_CONSTANTS>`
flag set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**draw\_list\_set\_push\_constant**(draw\_list: `int<class_int>`,
buffer: `PackedByteArray<class_PackedByteArray>`, size\_bytes:
`int<class_int>`)
`🔗<class_RenderingDevice_method_draw_list_set_push_constant>`

Sets the push constant data to `buffer` for the specified `draw_list`.
The shader determines how this binary data is used. The buffer's size in
bytes must also be specified in `size_bytes` (this can be obtained by
calling the `PackedByteArray.size<class_PackedByteArray_method_size>`
method on the passed `buffer`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **draw\_list\_switch\_to\_next\_pass**()
`🔗<class_RenderingDevice_method_draw_list_switch_to_next_pass>`

Switches to the next draw pass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>`
**draw\_list\_switch\_to\_next\_pass\_split**(splits: `int<class_int>`)
`🔗<class_RenderingDevice_method_draw_list_switch_to_next_pass_split>`

**Deprecated:** Split draw lists are used automatically by
RenderingDevice.

This method does nothing and always returns an empty
`PackedInt64Array<class_PackedInt64Array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **framebuffer\_create**(textures:
`Array<class_Array>`\[`RID<class_RID>`\], validate\_with\_format:
`int<class_int>` = -1, view\_count: `int<class_int>` = 1)
`🔗<class_RenderingDevice_method_framebuffer_create>`

Creates a new framebuffer. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **framebuffer\_create\_empty**(size:
`Vector2i<class_Vector2i>`, samples:
`TextureSamples<enum_RenderingDevice_TextureSamples>` = 0,
validate\_with\_format: `int<class_int>` = -1)
`🔗<class_RenderingDevice_method_framebuffer_create_empty>`

Creates a new empty framebuffer. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **framebuffer\_create\_multipass**(textures:
`Array<class_Array>`\[`RID<class_RID>`\], passes:
`Array<class_Array>`\[`RDFramebufferPass<class_RDFramebufferPass>`\],
validate\_with\_format: `int<class_int>` = -1, view\_count:
`int<class_int>` = 1)
`🔗<class_RenderingDevice_method_framebuffer_create_multipass>`

Creates a new multipass framebuffer. It can be accessed with the RID
that is returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **framebuffer\_format\_create**(attachments:
`Array<class_Array>`\[`RDAttachmentFormat<class_RDAttachmentFormat>`\],
view\_count: `int<class_int>` = 1)
`🔗<class_RenderingDevice_method_framebuffer_format_create>`

Creates a new framebuffer format with the specified `attachments` and
`view_count`. Returns the new framebuffer's unique framebuffer format
ID.

If `view_count` is greater than or equal to `2`, enables multiview which
is used for VR rendering. This requires support for the Vulkan multiview
extension.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **framebuffer\_format\_create\_empty**(samples:
`TextureSamples<enum_RenderingDevice_TextureSamples>` = 0)
`🔗<class_RenderingDevice_method_framebuffer_format_create_empty>`

Creates a new empty framebuffer format with the specified number of
`samples` and returns its ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **framebuffer\_format\_create\_multipass**(attachments:
`Array<class_Array>`\[`RDAttachmentFormat<class_RDAttachmentFormat>`\],
passes:
`Array<class_Array>`\[`RDFramebufferPass<class_RDFramebufferPass>`\],
view\_count: `int<class_int>` = 1)
`🔗<class_RenderingDevice_method_framebuffer_format_create_multipass>`

Creates a multipass framebuffer format with the specified `attachments`,
`passes` and `view_count` and returns its ID. If `view_count` is greater
than or equal to `2`, enables multiview which is used for VR rendering.
This requires support for the Vulkan multiview extension.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TextureSamples<enum_RenderingDevice_TextureSamples>`
**framebuffer\_format\_get\_texture\_samples**(format: `int<class_int>`,
render\_pass: `int<class_int>` = 0)
`🔗<class_RenderingDevice_method_framebuffer_format_get_texture_samples>`

Returns the number of texture samples used for the given framebuffer
`format` ID (returned by
`framebuffer_get_format<class_RenderingDevice_method_framebuffer_get_format>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **framebuffer\_get\_format**(framebuffer:
`RID<class_RID>`)
`🔗<class_RenderingDevice_method_framebuffer_get_format>`

Returns the format ID of the framebuffer specified by the `framebuffer`
RID. This ID is guaranteed to be unique for the same formats and does
not need to be freed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **framebuffer\_is\_valid**(framebuffer:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_framebuffer_is_valid>`

Returns `true` if the framebuffer specified by the `framebuffer` RID is
valid, `false` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **free\_rid**(rid: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_free_rid>`

Tries to free an object in the RenderingDevice. To avoid memory leaks,
this should be called after using an object as memory management does
not occur automatically when using RenderingDevice directly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **full\_barrier**()
`🔗<class_RenderingDevice_method_full_barrier>`

**Deprecated:** Barriers are automatically inserted by RenderingDevice.

This method does nothing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_captured\_timestamp\_cpu\_time**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_captured_timestamp_cpu_time>`

Returns the timestamp in CPU time for the rendering step specified by
`index` (in microseconds since the engine started). See also
`get_captured_timestamp_gpu_time<class_RenderingDevice_method_get_captured_timestamp_gpu_time>`
and `capture_timestamp<class_RenderingDevice_method_capture_timestamp>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_captured\_timestamp\_gpu\_time**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_captured_timestamp_gpu_time>`

Returns the timestamp in GPU time for the rendering step specified by
`index` (in microseconds since the engine started). See also
`get_captured_timestamp_cpu_time<class_RenderingDevice_method_get_captured_timestamp_cpu_time>`
and `capture_timestamp<class_RenderingDevice_method_capture_timestamp>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_captured\_timestamp\_name**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_captured_timestamp_name>`

Returns the timestamp's name for the rendering step specified by
`index`. See also
`capture_timestamp<class_RenderingDevice_method_capture_timestamp>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_captured\_timestamps\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_captured_timestamps_count>`

Returns the total number of timestamps (rendering steps) available for
profiling.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_captured\_timestamps\_frame**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_captured_timestamps_frame>`

Returns the index of the last frame rendered that has rendering
timestamps available for querying.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_device\_allocation\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_device_allocation_count>`

Returns how many allocations the GPU has performed for internal driver
structures.

This is only used by Vulkan in debug builds and can return 0 when this
information is not tracked or unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_device\_allocs\_by\_object\_type**(type:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_device_allocs_by_object_type>`

Same as
`get_device_allocation_count<class_RenderingDevice_method_get_device_allocation_count>`
but filtered for a given object type.

The type argument must be in range
`[0; get_tracked_object_type_count - 1]`. If
`get_tracked_object_type_count<class_RenderingDevice_method_get_tracked_object_type_count>`
is 0, then type argument is ignored and always returns 0.

This is only used by Vulkan in debug builds and can return 0 when this
information is not tracked or unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_device\_memory\_by\_object\_type**(type:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_device_memory_by_object_type>`

Same as
`get_device_total_memory<class_RenderingDevice_method_get_device_total_memory>`
but filtered for a given object type.

The type argument must be in range
`[0; get_tracked_object_type_count - 1]`. If
`get_tracked_object_type_count<class_RenderingDevice_method_get_tracked_object_type_count>`
is 0, then type argument is ignored and always returns 0.

This is only used by Vulkan in debug builds and can return 0 when this
information is not tracked or unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_device\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_device_name>`

Returns the name of the video adapter (e.g. "GeForce GTX
1080/PCIe/SSE2"). Equivalent to
`RenderingServer.get_video_adapter_name<class_RenderingServer_method_get_video_adapter_name>`.
See also
`get_device_vendor_name<class_RenderingDevice_method_get_device_vendor_name>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_device\_pipeline\_cache\_uuid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_device_pipeline_cache_uuid>`

Returns the universally unique identifier for the pipeline cache. This
is used to cache shader files on disk, which avoids shader
recompilations on subsequent engine runs. This UUID varies depending on
the graphics card model, but also the driver version. Therefore,
updating graphics drivers will invalidate the shader cache.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_device\_total\_memory**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_device_total_memory>`

Returns how much bytes the GPU is using.

This is only used by Vulkan in debug builds and can return 0 when this
information is not tracked or unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_device\_vendor\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_device_vendor_name>`

Returns the vendor of the video adapter (e.g. "NVIDIA Corporation").
Equivalent to
`RenderingServer.get_video_adapter_vendor<class_RenderingServer_method_get_video_adapter_vendor>`.
See also
`get_device_name<class_RenderingDevice_method_get_device_name>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_driver\_allocation\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_driver_allocation_count>`

Returns how many allocations the GPU driver has performed for internal
driver structures.

This is only used by Vulkan in debug builds and can return 0 when this
information is not tracked or unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_driver\_allocs\_by\_object\_type**(type:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_driver_allocs_by_object_type>`

Same as
`get_driver_allocation_count<class_RenderingDevice_method_get_driver_allocation_count>`
but filtered for a given object type.

The type argument must be in range
`[0; get_tracked_object_type_count - 1]`. If
`get_tracked_object_type_count<class_RenderingDevice_method_get_tracked_object_type_count>`
is 0, then type argument is ignored and always returns 0.

This is only used by Vulkan in debug builds and can return 0 when this
information is not tracked or unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_driver\_and\_device\_memory\_report**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_driver_and_device_memory_report>`

Returns string report in CSV format using the following methods:

-   `get_tracked_object_name<class_RenderingDevice_method_get_tracked_object_name>`
-   `get_tracked_object_type_count<class_RenderingDevice_method_get_tracked_object_type_count>`
-   `get_driver_total_memory<class_RenderingDevice_method_get_driver_total_memory>`
-   `get_driver_allocation_count<class_RenderingDevice_method_get_driver_allocation_count>`
-   `get_driver_memory_by_object_type<class_RenderingDevice_method_get_driver_memory_by_object_type>`
-   `get_driver_allocs_by_object_type<class_RenderingDevice_method_get_driver_allocs_by_object_type>`
-   `get_device_total_memory<class_RenderingDevice_method_get_device_total_memory>`
-   `get_device_allocation_count<class_RenderingDevice_method_get_device_allocation_count>`
-   `get_device_memory_by_object_type<class_RenderingDevice_method_get_device_memory_by_object_type>`
-   `get_device_allocs_by_object_type<class_RenderingDevice_method_get_device_allocs_by_object_type>`

This is only used by Vulkan in debug builds. Godot must also be started
with the `--extra-gpu-memory-tracking`
`command line argument <../tutorials/editor/command_line_tutorial>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_driver\_memory\_by\_object\_type**(type:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_driver_memory_by_object_type>`

Same as
`get_driver_total_memory<class_RenderingDevice_method_get_driver_total_memory>`
but filtered for a given object type.

The type argument must be in range
`[0; get_tracked_object_type_count - 1]`. If
`get_tracked_object_type_count<class_RenderingDevice_method_get_tracked_object_type_count>`
is 0, then type argument is ignored and always returns 0.

This is only used by Vulkan in debug builds and can return 0 when this
information is not tracked or unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_driver\_resource**(resource:
`DriverResource<enum_RenderingDevice_DriverResource>`, rid:
`RID<class_RID>`, index: `int<class_int>`)
`🔗<class_RenderingDevice_method_get_driver_resource>`

Returns the unique identifier of the driver `resource` for the specified
`rid`. Some driver resource types ignore the specified `rid` (see
`DriverResource<enum_RenderingDevice_DriverResource>` descriptions).
`index` is always ignored but must be specified anyway.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_driver\_total\_memory**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_driver_total_memory>`

Returns how much bytes the GPU driver is using for internal driver
structures.

This is only used by Vulkan in debug builds and can return 0 when this
information is not tracked or unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_frame\_delay**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_frame_delay>`

Returns the frame count kept by the graphics API. Higher values result
in higher input lag, but with more consistent throughput. For the main
**RenderingDevice**, frames are cycled (usually 3 with triple-buffered
V-Sync enabled). However, local **RenderingDevice**s only have 1 frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_memory\_usage**(type:
`MemoryType<enum_RenderingDevice_MemoryType>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_memory_usage>`

Returns the memory usage in bytes corresponding to the given `type`.
When using Vulkan, these statistics are calculated by [Vulkan Memory
Allocator](https://github.com/GPUOpen-LibrariesAndSDKs/VulkanMemoryAllocator).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_perf\_report**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_perf_report>`

Returns a string with a performance report from the past frame. Updates
every frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tracked\_object\_name**(type\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_tracked_object_name>`

Returns the name of the type of object for the given `type_index`. This
value must be in range `[0; get_tracked_object_type_count - 1]`. If
`get_tracked_object_type_count<class_RenderingDevice_method_get_tracked_object_type_count>`
is 0, then type argument is ignored and always returns the same string.

The return value is important because it gives meaning to the types
passed to
`get_driver_memory_by_object_type<class_RenderingDevice_method_get_driver_memory_by_object_type>`,
`get_driver_allocs_by_object_type<class_RenderingDevice_method_get_driver_allocs_by_object_type>`,
`get_device_memory_by_object_type<class_RenderingDevice_method_get_device_memory_by_object_type>`,
and
`get_device_allocs_by_object_type<class_RenderingDevice_method_get_device_allocs_by_object_type>`.
Examples of strings it can return (not exhaustive):

-   DEVICE\_MEMORY
-   PIPELINE\_CACHE
-   SWAPCHAIN\_KHR
-   COMMAND\_POOL

Thus if e.g. `get_tracked_object_name(5)` returns "COMMAND\_POOL", then
`get_device_memory_by_object_type(5)` returns the bytes used by the GPU
for command pools.

This is only used by Vulkan in debug builds. Godot must also be started
with the `--extra-gpu-memory-tracking`
`command line argument <../tutorials/editor/command_line_tutorial>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_tracked\_object\_type\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_get_tracked_object_type_count>`

Returns how many types of trackable objects are.

This is only used by Vulkan in debug builds. Godot must also be started
with the `--extra-gpu-memory-tracking`
`command line argument <../tutorials/editor/command_line_tutorial>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **index\_array\_create**(index\_buffer:
`RID<class_RID>`, index\_offset: `int<class_int>`, index\_count:
`int<class_int>`) `🔗<class_RenderingDevice_method_index_array_create>`

Creates a new index array. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **index\_buffer\_create**(size\_indices:
`int<class_int>`, format:
`IndexBufferFormat<enum_RenderingDevice_IndexBufferFormat>`, data:
`PackedByteArray<class_PackedByteArray>` = PackedByteArray(),
use\_restart\_indices: `bool<class_bool>` = false)
`🔗<class_RenderingDevice_method_index_buffer_create>`

Creates a new index buffer. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **limit\_get**(limit:
`Limit<enum_RenderingDevice_Limit>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_limit_get>`

Returns the value of the specified `limit`. This limit varies depending
on the current graphics hardware (and sometimes the driver version). If
the given limit is exceeded, rendering errors will occur.

Limits for various graphics hardware can be found in the [Vulkan
Hardware Database](https://vulkan.gpuinfo.org/).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **render\_pipeline\_create**(shader: `RID<class_RID>`,
framebuffer\_format: `int<class_int>`, vertex\_format: `int<class_int>`,
primitive: `RenderPrimitive<enum_RenderingDevice_RenderPrimitive>`,
rasterization\_state:
`RDPipelineRasterizationState<class_RDPipelineRasterizationState>`,
multisample\_state:
`RDPipelineMultisampleState<class_RDPipelineMultisampleState>`,
stencil\_state:
`RDPipelineDepthStencilState<class_RDPipelineDepthStencilState>`,
color\_blend\_state:
`RDPipelineColorBlendState<class_RDPipelineColorBlendState>`,
dynamic\_state\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`PipelineDynamicStateFlags<enum_RenderingDevice_PipelineDynamicStateFlags>`\]
= 0, for\_render\_pass: `int<class_int>` = 0, specialization\_constants:
`Array<class_Array>`\[`RDPipelineSpecializationConstant<class_RDPipelineSpecializationConstant>`\]
= \[\]) `🔗<class_RenderingDevice_method_render_pipeline_create>`

Creates a new render pipeline. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **render\_pipeline\_is\_valid**(render\_pipeline:
`RID<class_RID>`)
`🔗<class_RenderingDevice_method_render_pipeline_is_valid>`

Returns `true` if the render pipeline specified by the `render_pipeline`
RID is valid, `false` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **sampler\_create**(state:
`RDSamplerState<class_RDSamplerState>`)
`🔗<class_RenderingDevice_method_sampler_create>`

Creates a new sampler. It can be accessed with the RID that is returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**sampler\_is\_format\_supported\_for\_filter**(format:
`DataFormat<enum_RenderingDevice_DataFormat>`, sampler\_filter:
`SamplerFilter<enum_RenderingDevice_SamplerFilter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_sampler_is_format_supported_for_filter>`

Returns `true` if implementation supports using a texture of `format`
with the given `sampler_filter`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **screen\_get\_framebuffer\_format**(screen:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_screen_get_framebuffer_format>`

Returns the framebuffer format of the given screen.

\*\*Note:\*\* Only the main **RenderingDevice** returned by
`RenderingServer.get_rendering_device<class_RenderingServer_method_get_rendering_device>`
has a format. If called on a local **RenderingDevice**, this method
prints an error and returns
`INVALID_ID<class_RenderingDevice_constant_INVALID_ID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **screen\_get\_height**(screen: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_screen_get_height>`

Returns the window height matching the graphics API context for the
given window ID (in pixels). Despite the parameter being named `screen`,
this returns the *window* size. See also
`screen_get_width<class_RenderingDevice_method_screen_get_width>`.

\*\*Note:\*\* Only the main **RenderingDevice** returned by
`RenderingServer.get_rendering_device<class_RenderingServer_method_get_rendering_device>`
has a height. If called on a local **RenderingDevice**, this method
prints an error and returns
`INVALID_ID<class_RenderingDevice_constant_INVALID_ID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **screen\_get\_width**(screen: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_screen_get_width>`

Returns the window width matching the graphics API context for the given
window ID (in pixels). Despite the parameter being named `screen`, this
returns the *window* size. See also
`screen_get_height<class_RenderingDevice_method_screen_get_height>`.

\*\*Note:\*\* Only the main **RenderingDevice** returned by
`RenderingServer.get_rendering_device<class_RenderingServer_method_get_rendering_device>`
has a width. If called on a local **RenderingDevice**, this method
prints an error and returns
`INVALID_ID<class_RenderingDevice_constant_INVALID_ID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_resource\_name**(id: `RID<class_RID>`,
name: `String<class_String>`)
`🔗<class_RenderingDevice_method_set_resource_name>`

Sets the resource name for `id` to `name`. This is used for debugging
with third-party tools such as [RenderDoc](https://renderdoc.org/).

The following types of resources can be named: texture, sampler, vertex
buffer, index buffer, uniform buffer, texture buffer, storage buffer,
uniform set buffer, shader, render pipeline and compute pipeline.
Framebuffers cannot be named. Attempting to name an incompatible
resource type will print an error.

\*\*Note:\*\* Resource names are only set when the engine runs in
verbose mode (`OS.is_stdout_verbose<class_OS_method_is_stdout_verbose>`
= `true`), or when using an engine build compiled with the
`dev_mode=yes` SCons option. The graphics driver must also support the
`VK_EXT_DEBUG_UTILS_EXTENSION_NAME` Vulkan extension for named resources
to work.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**shader\_compile\_binary\_from\_spirv**(spirv\_data:
`RDShaderSPIRV<class_RDShaderSPIRV>`, name: `String<class_String>` = "")
`🔗<class_RenderingDevice_method_shader_compile_binary_from_spirv>`

Compiles a binary shader from `spirv_data` and returns the compiled
binary data as a `PackedByteArray<class_PackedByteArray>`. This compiled
shader is specific to the GPU model and driver version used; it will not
work on different GPU models or even different driver versions. See also
`shader_compile_spirv_from_source<class_RenderingDevice_method_shader_compile_spirv_from_source>`.

`name` is an optional human-readable name that can be given to the
compiled shader for organizational purposes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RDShaderSPIRV<class_RDShaderSPIRV>`
**shader\_compile\_spirv\_from\_source**(shader\_source:
`RDShaderSource<class_RDShaderSource>`, allow\_cache: `bool<class_bool>`
= true)
`🔗<class_RenderingDevice_method_shader_compile_spirv_from_source>`

Compiles a SPIR-V from the shader source code in `shader_source` and
returns the SPIR-V as a `RDShaderSPIRV<class_RDShaderSPIRV>`. This
intermediate language shader is portable across different GPU models and
driver versions, but cannot be run directly by GPUs until compiled into
a binary shader using
`shader_compile_binary_from_spirv<class_RenderingDevice_method_shader_compile_binary_from_spirv>`.

If `allow_cache` is `true`, make use of the shader cache generated by
Godot. This avoids a potentially lengthy shader compilation step if the
shader is already in cache. If `allow_cache` is `false`, Godot's shader
cache is ignored and the shader will always be recompiled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **shader\_create\_from\_bytecode**(binary\_data:
`PackedByteArray<class_PackedByteArray>`, placeholder\_rid:
`RID<class_RID>` = RID())
`🔗<class_RenderingDevice_method_shader_create_from_bytecode>`

Creates a new shader instance from a binary compiled shader. It can be
accessed with the RID that is returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method. See also
`shader_compile_binary_from_spirv<class_RenderingDevice_method_shader_compile_binary_from_spirv>`
and
`shader_create_from_spirv<class_RenderingDevice_method_shader_create_from_spirv>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **shader\_create\_from\_spirv**(spirv\_data:
`RDShaderSPIRV<class_RDShaderSPIRV>`, name: `String<class_String>` = "")
`🔗<class_RenderingDevice_method_shader_create_from_spirv>`

Creates a new shader instance from SPIR-V intermediate code. It can be
accessed with the RID that is returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method. See also
`shader_compile_spirv_from_source<class_RenderingDevice_method_shader_compile_spirv_from_source>`
and
`shader_create_from_bytecode<class_RenderingDevice_method_shader_create_from_bytecode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **shader\_create\_placeholder**()
`🔗<class_RenderingDevice_method_shader_create_placeholder>`

Create a placeholder RID by allocating an RID without initializing it
for use in
`shader_create_from_bytecode<class_RenderingDevice_method_shader_create_from_bytecode>`.
This allows you to create an RID for a shader and pass it around, but
defer compiling the shader to a later time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **shader\_get\_vertex\_input\_attribute\_mask**(shader:
`RID<class_RID>`)
`🔗<class_RenderingDevice_method_shader_get_vertex_input_attribute_mask>`

Returns the internal vertex input mask. Internally, the vertex input
mask is an unsigned integer consisting of the locations (specified in
GLSL via. `layout(location = ...)`) of the input variables (specified in
GLSL by the `in` keyword).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **storage\_buffer\_create**(size\_bytes:
`int<class_int>`, data: `PackedByteArray<class_PackedByteArray>` =
PackedByteArray(), usage:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`StorageBufferUsage<enum_RenderingDevice_StorageBufferUsage>`\]
= 0) `🔗<class_RenderingDevice_method_storage_buffer_create>`

Creates a [storage
buffer](https://vkguide.dev/docs/chapter-4/storage_buffers/) with the
specified `data` and `usage`. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **submit**()
`🔗<class_RenderingDevice_method_submit>`

Pushes the frame setup and draw command buffers then marks the local
device as currently processing (which allows calling
`sync<class_RenderingDevice_method_sync>`).

\*\*Note:\*\* Only available in local RenderingDevices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **sync**()
`🔗<class_RenderingDevice_method_sync>`

Forces a synchronization between the CPU and GPU, which may be required
in certain cases. Only call this when needed, as CPU-GPU synchronization
has a performance cost.

\*\*Note:\*\* Only available in local RenderingDevices.

\*\*Note:\*\* `sync<class_RenderingDevice_method_sync>` can only be
called after a `submit<class_RenderingDevice_method_submit>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_buffer\_create**(size\_bytes:
`int<class_int>`, format: `DataFormat<enum_RenderingDevice_DataFormat>`,
data: `PackedByteArray<class_PackedByteArray>` = PackedByteArray())
`🔗<class_RenderingDevice_method_texture_buffer_create>`

Creates a new texture buffer. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **texture\_clear**(texture:
`RID<class_RID>`, color: `Color<class_Color>`, base\_mipmap:
`int<class_int>`, mipmap\_count: `int<class_int>`, base\_layer:
`int<class_int>`, layer\_count: `int<class_int>`)
`🔗<class_RenderingDevice_method_texture_clear>`

Clears the specified `texture` by replacing all of its pixels with the
specified `color`. `base_mipmap` and `mipmap_count` determine which
mipmaps of the texture are affected by this clear operation, while
`base_layer` and `layer_count` determine which layers of a 3D texture
(or texture array) are affected by this clear operation. For 2D textures
(which only have one layer by design), `base_layer` must be `0` and
`layer_count` must be `1`.

\*\*Note:\*\* `texture` can't be cleared while a draw list that uses it
as part of a framebuffer is being created. Ensure the draw list is
finalized (and that the color/depth texture using it is not set to
`FINAL_ACTION_CONTINUE<class_RenderingDevice_constant_FINAL_ACTION_CONTINUE>`)
to clear this texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **texture\_copy**(from\_texture:
`RID<class_RID>`, to\_texture: `RID<class_RID>`, from\_pos:
`Vector3<class_Vector3>`, to\_pos: `Vector3<class_Vector3>`, size:
`Vector3<class_Vector3>`, src\_mipmap: `int<class_int>`, dst\_mipmap:
`int<class_int>`, src\_layer: `int<class_int>`, dst\_layer:
`int<class_int>`) `🔗<class_RenderingDevice_method_texture_copy>`

Copies the `from_texture` to `to_texture` with the specified `from_pos`,
`to_pos` and `size` coordinates. The Z axis of the `from_pos`, `to_pos`
and `size` must be `0` for 2-dimensional textures. Source and
destination mipmaps/layers must also be specified, with these parameters
being `0` for textures without mipmaps or single-layer textures. Returns
`@GlobalScope.OK<class_@GlobalScope_constant_OK>` if the texture copy
was successful or
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
otherwise.

\*\*Note:\*\* `from_texture` texture can't be copied while a draw list
that uses it as part of a framebuffer is being created. Ensure the draw
list is finalized (and that the color/depth texture using it is not set
to
`FINAL_ACTION_CONTINUE<class_RenderingDevice_constant_FINAL_ACTION_CONTINUE>`)
to copy this texture.

\*\*Note:\*\* `from_texture` texture requires the
`TEXTURE_USAGE_CAN_COPY_FROM_BIT<class_RenderingDevice_constant_TEXTURE_USAGE_CAN_COPY_FROM_BIT>`
to be retrieved.

\*\*Note:\*\* `to_texture` can't be copied while a draw list that uses
it as part of a framebuffer is being created. Ensure the draw list is
finalized (and that the color/depth texture using it is not set to
`FINAL_ACTION_CONTINUE<class_RenderingDevice_constant_FINAL_ACTION_CONTINUE>`)
to copy this texture.

\*\*Note:\*\* `to_texture` requires the
`TEXTURE_USAGE_CAN_COPY_TO_BIT<class_RenderingDevice_constant_TEXTURE_USAGE_CAN_COPY_TO_BIT>`
to be retrieved.

\*\*Note:\*\* `from_texture` and `to_texture` must be of the same type
(color or depth).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_create**(format:
`RDTextureFormat<class_RDTextureFormat>`, view:
`RDTextureView<class_RDTextureView>`, data:
`Array<class_Array>`\[`PackedByteArray<class_PackedByteArray>`\] = \[\])
`🔗<class_RenderingDevice_method_texture_create>`

Creates a new texture. It can be accessed with the RID that is returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

\*\*Note:\*\* Not to be confused with
`RenderingServer.texture_2d_create<class_RenderingServer_method_texture_2d_create>`,
which creates the Godot-specific `Texture2D<class_Texture2D>` resource
as opposed to the graphics API's own texture type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_create\_from\_extension**(type:
`TextureType<enum_RenderingDevice_TextureType>`, format:
`DataFormat<enum_RenderingDevice_DataFormat>`, samples:
`TextureSamples<enum_RenderingDevice_TextureSamples>`, usage\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`\],
image: `int<class_int>`, width: `int<class_int>`, height:
`int<class_int>`, depth: `int<class_int>`, layers: `int<class_int>`)
`🔗<class_RenderingDevice_method_texture_create_from_extension>`

Returns an RID for an existing `image` (`VkImage`) with the given
`type`, `format`, `samples`, `usage_flags`, `width`, `height`, `depth`,
and `layers`. This can be used to allow Godot to render onto foreign
images.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_create\_shared**(view:
`RDTextureView<class_RDTextureView>`, with\_texture: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_texture_create_shared>`

Creates a shared texture using the specified `view` and the texture
information from `with_texture`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **texture\_create\_shared\_from\_slice**(view:
`RDTextureView<class_RDTextureView>`, with\_texture: `RID<class_RID>`,
layer: `int<class_int>`, mipmap: `int<class_int>`, mipmaps:
`int<class_int>` = 1, slice\_type:
`TextureSliceType<enum_RenderingDevice_TextureSliceType>` = 0)
`🔗<class_RenderingDevice_method_texture_create_shared_from_slice>`

Creates a shared texture using the specified `view` and the texture
information from `with_texture`'s `layer` and `mipmap`. The number of
included mipmaps from the original texture can be controlled using the
`mipmaps` parameter. Only relevant for textures with multiple layers,
such as 3D textures, texture arrays and cubemaps. For single-layer
textures, use
`texture_create_shared<class_RenderingDevice_method_texture_create_shared>`.

For 2D textures (which only have one layer), `layer` must be `0`.

\*\*Note:\*\* Layer slicing is only supported for 2D texture arrays, not
3D textures or cubemaps.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **texture\_get\_data**(texture:
`RID<class_RID>`, layer: `int<class_int>`)
`🔗<class_RenderingDevice_method_texture_get_data>`

Returns the `texture` data for the specified `layer` as raw binary data.
For 2D textures (which only have one layer), `layer` must be `0`.

\*\*Note:\*\* `texture` can't be retrieved while a draw list that uses
it as part of a framebuffer is being created. Ensure the draw list is
finalized (and that the color/depth texture using it is not set to
`FINAL_ACTION_CONTINUE<class_RenderingDevice_constant_FINAL_ACTION_CONTINUE>`)
to retrieve this texture. Otherwise, an error is printed and a empty
`PackedByteArray<class_PackedByteArray>` is returned.

\*\*Note:\*\* `texture` requires the
`TEXTURE_USAGE_CAN_COPY_FROM_BIT<class_RenderingDevice_constant_TEXTURE_USAGE_CAN_COPY_FROM_BIT>`
to be retrieved. Otherwise, an error is printed and a empty
`PackedByteArray<class_PackedByteArray>` is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RDTextureFormat<class_RDTextureFormat>`
**texture\_get\_format**(texture: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_texture_get_format>`

Returns the data format used to create this texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **texture\_get\_native\_handle**(texture:
`RID<class_RID>`)
`🔗<class_RenderingDevice_method_texture_get_native_handle>`

**Deprecated:** Use
`get_driver_resource<class_RenderingDevice_method_get_driver_resource>`
with
`DRIVER_RESOURCE_TEXTURE<class_RenderingDevice_constant_DRIVER_RESOURCE_TEXTURE>`
instead.

Returns the internal graphics handle for this texture object. For use
when communicating with third-party APIs mostly with GDExtension.

\*\*Note:\*\* This function returns a `uint64_t` which internally maps
to a `GLuint` (OpenGL) or `VkImage` (Vulkan).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**texture\_is\_format\_supported\_for\_usage**(format:
`DataFormat<enum_RenderingDevice_DataFormat>`, usage\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`\])
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderingDevice_method_texture_is_format_supported_for_usage>`

Returns `true` if the specified `format` is supported for the given
`usage_flags`, `false` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **texture\_is\_shared**(texture: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_texture_is_shared>`

Returns `true` if the `texture` is shared, `false` otherwise. See
`RDTextureView<class_RDTextureView>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **texture\_is\_valid**(texture: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_texture_is_valid>`

Returns `true` if the `texture` is valid, `false` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**texture\_resolve\_multisample**(from\_texture: `RID<class_RID>`,
to\_texture: `RID<class_RID>`)
`🔗<class_RenderingDevice_method_texture_resolve_multisample>`

Resolves the `from_texture` texture onto `to_texture` with multisample
antialiasing enabled. This must be used when rendering a framebuffer for
MSAA to work. Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>`
if successful,
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
otherwise.

\*\*Note:\*\* `from_texture` and `to_texture` textures must have the
same dimension, format and type (color or depth).

\*\*Note:\*\* `from_texture` can't be copied while a draw list that uses
it as part of a framebuffer is being created. Ensure the draw list is
finalized (and that the color/depth texture using it is not set to
`FINAL_ACTION_CONTINUE<class_RenderingDevice_constant_FINAL_ACTION_CONTINUE>`)
to resolve this texture.

\*\*Note:\*\* `from_texture` requires the
`TEXTURE_USAGE_CAN_COPY_FROM_BIT<class_RenderingDevice_constant_TEXTURE_USAGE_CAN_COPY_FROM_BIT>`
to be retrieved.

\*\*Note:\*\* `from_texture` must be multisampled and must also be 2D
(or a slice of a 3D/cubemap texture).

\*\*Note:\*\* `to_texture` can't be copied while a draw list that uses
it as part of a framebuffer is being created. Ensure the draw list is
finalized (and that the color/depth texture using it is not set to
`FINAL_ACTION_CONTINUE<class_RenderingDevice_constant_FINAL_ACTION_CONTINUE>`)
to resolve this texture.

\*\*Note:\*\* `to_texture` texture requires the
`TEXTURE_USAGE_CAN_COPY_TO_BIT<class_RenderingDevice_constant_TEXTURE_USAGE_CAN_COPY_TO_BIT>`
to be retrieved.

\*\*Note:\*\* `to_texture` texture must **not** be multisampled and must
also be 2D (or a slice of a 3D/cubemap texture).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **texture\_update**(texture:
`RID<class_RID>`, layer: `int<class_int>`, data:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_RenderingDevice_method_texture_update>`

Updates texture data with new data, replacing the previous data in
place. The updated texture data must have the same dimensions and
format. For 2D textures (which only have one layer), `layer` must be
`0`. Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` if the
update was successful,
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
otherwise.

\*\*Note:\*\* Updating textures is forbidden during creation of a draw
or compute list.

\*\*Note:\*\* The existing `texture` can't be updated while a draw list
that uses it as part of a framebuffer is being created. Ensure the draw
list is finalized (and that the color/depth texture using it is not set
to
`FINAL_ACTION_CONTINUE<class_RenderingDevice_constant_FINAL_ACTION_CONTINUE>`)
to update this texture.

\*\*Note:\*\* The existing `texture` requires the
`TEXTURE_USAGE_CAN_UPDATE_BIT<class_RenderingDevice_constant_TEXTURE_USAGE_CAN_UPDATE_BIT>`
to be updatable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **uniform\_buffer\_create**(size\_bytes:
`int<class_int>`, data: `PackedByteArray<class_PackedByteArray>` =
PackedByteArray())
`🔗<class_RenderingDevice_method_uniform_buffer_create>`

Creates a new uniform buffer. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **uniform\_set\_create**(uniforms:
`Array<class_Array>`\[`RDUniform<class_RDUniform>`\], shader:
`RID<class_RID>`, shader\_set: `int<class_int>`)
`🔗<class_RenderingDevice_method_uniform_set_create>`

Creates a new uniform set. It can be accessed with the RID that is
returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **uniform\_set\_is\_valid**(uniform\_set:
`RID<class_RID>`)
`🔗<class_RenderingDevice_method_uniform_set_is_valid>`

Checks if the `uniform_set` is valid, i.e. is owned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **vertex\_array\_create**(vertex\_count:
`int<class_int>`, vertex\_format: `int<class_int>`, src\_buffers:
`Array<class_Array>`\[`RID<class_RID>`\], offsets:
`PackedInt64Array<class_PackedInt64Array>` = PackedInt64Array())
`🔗<class_RenderingDevice_method_vertex_array_create>`

Creates a vertex array based on the specified buffers. Optionally,
`offsets` (in bytes) may be defined for each buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **vertex\_buffer\_create**(size\_bytes:
`int<class_int>`, data: `PackedByteArray<class_PackedByteArray>` =
PackedByteArray(), use\_as\_storage: `bool<class_bool>` = false)
`🔗<class_RenderingDevice_method_vertex_buffer_create>`

It can be accessed with the RID that is returned.

Once finished with your RID, you will want to free the RID using the
RenderingDevice's `free_rid<class_RenderingDevice_method_free_rid>`
method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **vertex\_format\_create**(vertex\_descriptions:
`Array<class_Array>`\[`RDVertexAttribute<class_RDVertexAttribute>`\])
`🔗<class_RenderingDevice_method_vertex_format_create>`

Creates a new vertex format with the specified `vertex_descriptions`.
Returns a unique vertex format ID corresponding to the newly created
vertex format.
