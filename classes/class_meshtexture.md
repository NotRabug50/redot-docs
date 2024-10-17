github\_url  
hide

# MeshTexture

**Inherits:** `Texture2D<class_Texture2D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Simple texture that uses a mesh to draw itself.

classref-introduction-group

## Description

Simple texture that uses a mesh to draw itself. It's limited because
flags can't be changed and region drawing is not supported.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Texture2D<class_Texture2D>` **base\_texture**
`🔗<class_MeshTexture_property_base_texture>`

classref-property-setget

-   `void (No return value.)` **set\_base\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_base\_texture**()

Sets the base texture that the Mesh will use to draw.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **image\_size** = `Vector2(0, 0)`
`🔗<class_MeshTexture_property_image_size>`

classref-property-setget

-   `void (No return value.)` **set\_image\_size**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_image\_size**()

Sets the size of the image, needed for reference.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mesh<class_Mesh>` **mesh** `🔗<class_MeshTexture_property_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_mesh**(value: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_mesh**()

Sets the mesh used to draw. It must be a mesh using 2D vertices.
