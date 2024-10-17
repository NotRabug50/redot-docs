github\_url  
hide

# Texture3DRD

**Inherits:** `Texture3D<class_Texture3D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Texture for 3D that is bound to a texture created on the
`RenderingDevice<class_RenderingDevice>`.

classref-introduction-group

## Description

This texture class allows you to use a 3D texture created directly on
the `RenderingDevice<class_RenderingDevice>` as a texture for materials,
meshes, etc.

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

`RID<class_RID>` **texture\_rd\_rid**
`🔗<class_Texture3DRD_property_texture_rd_rid>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_rd\_rid**(value:
    `RID<class_RID>`)
-   `RID<class_RID>` **get\_texture\_rd\_rid**()

The RID of the texture object created on the
`RenderingDevice<class_RenderingDevice>`.
