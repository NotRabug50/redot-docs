github\_url  
hide

# GLTFSpecGloss

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Archived glTF extension for specular/glossy materials.

classref-introduction-group

## Description

KHR\_materials\_pbrSpecularGlossiness is an archived glTF extension.
This means that it is deprecated and not recommended for new files.
However, it is still supported for loading old files.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [KHR\_materials\_pbrSpecularGlossiness glTF extension
    spec](https://github.com/KhronosGroup/glTF/blob/main/extensions/2.0/Archived/KHR_materials_pbrSpecularGlossiness)

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

## Property Descriptions

classref-property

`Color<class_Color>` **diffuse\_factor** = `Color(1, 1, 1, 1)`
`🔗<class_GLTFSpecGloss_property_diffuse_factor>`

classref-property-setget

-   `void (No return value.)` **set\_diffuse\_factor**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_diffuse\_factor**()

The reflected diffuse factor of the material.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Image<class_Image>` **diffuse\_img**
`🔗<class_GLTFSpecGloss_property_diffuse_img>`

classref-property-setget

-   `void (No return value.)` **set\_diffuse\_img**(value:
    `Image<class_Image>`)
-   `Image<class_Image>` **get\_diffuse\_img**()

The diffuse texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gloss\_factor** = `1.0`
`🔗<class_GLTFSpecGloss_property_gloss_factor>`

classref-property-setget

-   `void (No return value.)` **set\_gloss\_factor**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_gloss\_factor**()

The glossiness or smoothness of the material.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Image<class_Image>` **spec\_gloss\_img**
`🔗<class_GLTFSpecGloss_property_spec_gloss_img>`

classref-property-setget

-   `void (No return value.)` **set\_spec\_gloss\_img**(value:
    `Image<class_Image>`)
-   `Image<class_Image>` **get\_spec\_gloss\_img**()

The specular-glossiness texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **specular\_factor** = `Color(1, 1, 1, 1)`
`🔗<class_GLTFSpecGloss_property_specular_factor>`

classref-property-setget

-   `void (No return value.)` **set\_specular\_factor**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_specular\_factor**()

The specular RGB color of the material. The alpha channel is unused.
