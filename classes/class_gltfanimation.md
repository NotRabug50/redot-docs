github\_url  
hide

# GLTFAnimation

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

There is currently no description for this class. Please help us by
`contributing one <doc_updating_the_class_reference>`!

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

`bool<class_bool>` **loop** = `false`
`🔗<class_GLTFAnimation_property_loop>`

classref-property-setget

-   `void (No return value.)` **set\_loop**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_loop**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **original\_name** = `""`
`🔗<class_GLTFAnimation_property_original_name>`

classref-property-setget

-   `void (No return value.)` **set\_original\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_original\_name**()

The original name of the animation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Variant<class_Variant>` **get\_additional\_data**(extension\_name:
`StringName<class_StringName>`)
`🔗<class_GLTFAnimation_method_get_additional_data>`

Gets additional arbitrary data in this **GLTFAnimation** instance. This
can be used to keep per-node state data in
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes, which is
important because they are stateless.

The argument should be the
`GLTFDocumentExtension<class_GLTFDocumentExtension>` name (does not have
to match the extension name in the glTF file), and the return value can
be anything you set. If nothing was set, the return value is null.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_additional\_data**(extension\_name:
`StringName<class_StringName>`, additional\_data:
`Variant<class_Variant>`)
`🔗<class_GLTFAnimation_method_set_additional_data>`

Sets additional arbitrary data in this **GLTFAnimation** instance. This
can be used to keep per-node state data in
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes, which is
important because they are stateless.

The first argument should be the
`GLTFDocumentExtension<class_GLTFDocumentExtension>` name (does not have
to match the extension name in the glTF file), and the second argument
can be anything you want.
