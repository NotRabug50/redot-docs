github\_url  
hide

# RenderSceneBuffers

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

**Inherited By:**
`RenderSceneBuffersExtension<class_RenderSceneBuffersExtension>`,
`RenderSceneBuffersRD<class_RenderSceneBuffersRD>`

Abstract scene buffers object, created for each viewport for which 3D
rendering is done.

classref-introduction-group

## Description

Abstract scene buffers object, created for each viewport for which 3D
rendering is done. It manages any additional buffers used during
rendering and will discard buffers when the viewport is resized.

\*\*Note:\*\* This is an internal rendering server object, do not
instantiate this from script.

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **configure**(config:
`RenderSceneBuffersConfiguration<class_RenderSceneBuffersConfiguration>`)
`🔗<class_RenderSceneBuffers_method_configure>`

This method is called by the rendering server when the associated
viewports configuration is changed. It will discard the old buffers and
recreate the internal buffers used.
