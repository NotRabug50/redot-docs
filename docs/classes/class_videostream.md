github\_url  
hide

# VideoStream

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `VideoStreamTheora<class_VideoStreamTheora>`

Base resource for video streams.

classref-introduction-group

## Description

Base resource type for all video streams. Classes that derive from
**VideoStream** can all be used as resource types to play back videos in
`VideoStreamPlayer<class_VideoStreamPlayer>`.

classref-introduction-group

## Tutorials

-   `Playing videos <../tutorials/animation/playing_videos>`
-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`

classref-reftable-group

## Properties

<table>
<tbody>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **file** = `""`
`🔗<class_VideoStream_property_file>`

classref-property-setget

-   `void (No return value.)` **set\_file**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_file**()

The video file path or URI that this **VideoStream** resource handles.

For `VideoStreamTheora<class_VideoStreamTheora>`, this filename should
be an Ogg Theora video file with the `.ogv` extension.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`VideoStreamPlayback<class_VideoStreamPlayback>`
**\_instantiate\_playback**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_VideoStream_private_method__instantiate_playback>`

Called when the video starts playing, to initialize and return a
subclass of `VideoStreamPlayback<class_VideoStreamPlayback>`.
