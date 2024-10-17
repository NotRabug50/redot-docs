github\_url  
hide

# ExternalTexture

**Inherits:** `Texture2D<class_Texture2D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Texture which displays the content of an external buffer.

classref-introduction-group

## Description

Displays the content of an external buffer provided by the platform.

Requires the
[OES\_EGL\_image\_external](https://registry.khronos.org/OpenGL/extensions/OES/OES_EGL_image_external.txt)
extension (OpenGL) or
[VK\_ANDROID\_external\_memory\_android\_hardware\_buffer](https://registry.khronos.org/vulkan/specs/1.1-extensions/html/vkspec.html#VK_ANDROID_external_memory_android_hardware_buffer)
extension (Vulkan).

\*\*Note:\*\* This is currently only supported in Android builds.

classref-reftable-group

## Properties

<table>
<tbody>
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

## Property Descriptions

classref-property

`Vector2<class_Vector2>` **size** = `Vector2(256, 256)`
`🔗<class_ExternalTexture_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_size**()

External texture size.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_external\_texture\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ExternalTexture_method_get_external_texture_id>`

Returns the external texture ID.

Depending on your use case, you may need to pass this to platform APIs,
for example, when creating an `android.graphics.SurfaceTexture` on
Android.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_external\_buffer\_id**(external\_buffer\_id: `int<class_int>`)
`🔗<class_ExternalTexture_method_set_external_buffer_id>`

Sets the external buffer ID.

Depending on your use case, you may need to call this with data received
from a platform API, for example, `SurfaceTexture.getHardwareBuffer()`
on Android.
