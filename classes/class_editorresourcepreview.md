github\_url  
hide

# EditorResourcePreview

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

A node used to generate previews of resources or files.

classref-introduction-group

## Description

This node is used to generate previews for resources or files.

\*\*Note:\*\* This class shouldn't be instantiated directly. Instead,
access the singleton using
`EditorInterface.get_resource_previewer<class_EditorInterface_method_get_resource_previewer>`.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**preview\_invalidated**(path: `String<class_String>`)
`🔗<class_EditorResourcePreview_signal_preview_invalidated>`

Emitted if a preview was invalidated (changed). `path` corresponds to
the path of the preview.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_preview\_generator**(generator:
`EditorResourcePreviewGenerator<class_EditorResourcePreviewGenerator>`)
`🔗<class_EditorResourcePreview_method_add_preview_generator>`

Create an own, custom preview generator.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **check\_for\_invalidation**(path:
`String<class_String>`)
`🔗<class_EditorResourcePreview_method_check_for_invalidation>`

Check if the resource changed, if so, it will be invalidated and the
corresponding signal emitted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **queue\_edited\_resource\_preview**(resource:
`Resource<class_Resource>`, receiver: `Object<class_Object>`,
receiver\_func: `StringName<class_StringName>`, userdata:
`Variant<class_Variant>`)
`🔗<class_EditorResourcePreview_method_queue_edited_resource_preview>`

Queue the `resource` being edited for preview. Once the preview is
ready, the `receiver`'s `receiver_func` will be called. The
`receiver_func` must take the following four arguments:
`String<class_String>` path, `Texture2D<class_Texture2D>` preview,
`Texture2D<class_Texture2D>` thumbnail\_preview,
`Variant<class_Variant>` userdata. `userdata` can be anything, and will
be returned when `receiver_func` is called.

\*\*Note:\*\* If it was not possible to create the preview the
`receiver_func` will still be called, but the preview will be null.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **queue\_resource\_preview**(path:
`String<class_String>`, receiver: `Object<class_Object>`,
receiver\_func: `StringName<class_StringName>`, userdata:
`Variant<class_Variant>`)
`🔗<class_EditorResourcePreview_method_queue_resource_preview>`

Queue a resource file located at `path` for preview. Once the preview is
ready, the `receiver`'s `receiver_func` will be called. The
`receiver_func` must take the following four arguments:
`String<class_String>` path, `Texture2D<class_Texture2D>` preview,
`Texture2D<class_Texture2D>` thumbnail\_preview,
`Variant<class_Variant>` userdata. `userdata` can be anything, and will
be returned when `receiver_func` is called.

\*\*Note:\*\* If it was not possible to create the preview the
`receiver_func` will still be called, but the preview will be null.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_preview\_generator**(generator:
`EditorResourcePreviewGenerator<class_EditorResourcePreviewGenerator>`)
`🔗<class_EditorResourcePreview_method_remove_preview_generator>`

Removes a custom preview generator.
