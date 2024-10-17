github\_url  
hide

# RenderSceneBuffersExtension

**Inherits:** `RenderSceneBuffers<class_RenderSceneBuffers>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

This class allows for a RenderSceneBuffer implementation to be made in
GDExtension.

classref-introduction-group

## Description

This class allows for a RenderSceneBuffer implementation to be made in
GDExtension.

classref-reftable-group

## Methods

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

## Method Descriptions

classref-method

`void (No return value.)` **\_configure**(config:
`RenderSceneBuffersConfiguration<class_RenderSceneBuffersConfiguration>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_RenderSceneBuffersExtension_private_method__configure>`

Implement this in GDExtension to handle the (re)sizing of a viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_fsr\_sharpness**(fsr\_sharpness:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_RenderSceneBuffersExtension_private_method__set_fsr_sharpness>`

Implement this in GDExtension to record a new FSR sharpness value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_set\_texture\_mipmap\_bias**(texture\_mipmap\_bias:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_RenderSceneBuffersExtension_private_method__set_texture_mipmap_bias>`

Implement this in GDExtension to change the texture mipmap bias.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_use\_debanding**(use\_debanding:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_RenderSceneBuffersExtension_private_method__set_use_debanding>`

Implement this in GDExtension to react to the debanding flag changing.
