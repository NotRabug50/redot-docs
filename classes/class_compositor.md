github\_url  
hide

# Compositor

**Experimental:** More customization of the rendering pipeline will be
added in the future.

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Stores attributes used to customize how a Viewport is rendered.

classref-introduction-group

## Description

The compositor resource stores attributes used to customize how a
`Viewport<class_Viewport>` is rendered.

classref-introduction-group

## Tutorials

-   `The Compositor <../tutorials/rendering/compositor>`

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

`Array<class_Array>`\[`CompositorEffect<class_CompositorEffect>`\]
**compositor\_effects** = `[]`
`🔗<class_Compositor_property_compositor_effects>`

classref-property-setget

-   `void (No return value.)` **set\_compositor\_effects**(value:
    `Array<class_Array>`\[`CompositorEffect<class_CompositorEffect>`\])
-   `Array<class_Array>`\[`CompositorEffect<class_CompositorEffect>`\]
    **get\_compositor\_effects**()

The custom `CompositorEffect<class_CompositorEffect>`s that are applied
during rendering of viewports using this compositor.
