github\_url  
hide

# GLTFTexture

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

GLTFTexture represents a texture in a glTF file.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **sampler** = `-1`
`🔗<class_GLTFTexture_property_sampler>`

classref-property-setget

-   `void (No return value.)` **set\_sampler**(value: `int<class_int>`)
-   `int<class_int>` **get\_sampler**()

ID of the texture sampler to use when sampling the image. If -1, then
the default texture sampler is used (linear filtering, and repeat
wrapping in both axes).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **src\_image** = `-1`
`🔗<class_GLTFTexture_property_src_image>`

classref-property-setget

-   `void (No return value.)` **set\_src\_image**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_src\_image**()

The index of the image associated with this texture, see
`GLTFState.get_images<class_GLTFState_method_get_images>`. If -1, then
this texture does not have an image assigned.
