github\_url  
hide

# PlaceholderTexture3D

**Inherits:** `Texture3D<class_Texture3D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Placeholder class for a 3-dimensional texture.

classref-introduction-group

## Description

This class is used when loading a project that uses a
`Texture3D<class_Texture3D>` subclass in 2 conditions:

-   When running the project exported in dedicated server mode, only the
    texture's dimensions are kept (as they may be relied upon for
    gameplay purposes or positioning of other elements). This allows
    reducing the exported PCK's size significantly.
-   When this subclass is missing due to using a different engine
    version or build (e.g. modules disabled).

\*\*Note:\*\* This is not intended to be used as an actual texture for
rendering. It is not guaranteed to work like one in shaders or materials
(for example when calculating UV).

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector3i<class_Vector3i>` **size** = `Vector3i(1, 1, 1)`
`🔗<class_PlaceholderTexture3D_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3i<class_Vector3i>`)
-   `Vector3i<class_Vector3i>` **get\_size**()

The texture's size (in pixels).
