github\_url  
hide

# TextureLayeredRD

**Inherits:** `TextureLayered<class_TextureLayered>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `Texture2DArrayRD<class_Texture2DArrayRD>`,
`TextureCubemapArrayRD<class_TextureCubemapArrayRD>`,
`TextureCubemapRD<class_TextureCubemapRD>`

Abstract base class for layered texture RD types.

classref-introduction-group

## Description

Base class for `Texture2DArrayRD<class_Texture2DArrayRD>`,
`TextureCubemapRD<class_TextureCubemapRD>` and
`TextureCubemapArrayRD<class_TextureCubemapArrayRD>`. Cannot be used
directly, but contains all the functions necessary for accessing the
derived resource types.

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
`🔗<class_TextureLayeredRD_property_texture_rd_rid>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_rd\_rid**(value:
    `RID<class_RID>`)
-   `RID<class_RID>` **get\_texture\_rd\_rid**()

The RID of the texture object created on the
`RenderingDevice<class_RenderingDevice>`.
