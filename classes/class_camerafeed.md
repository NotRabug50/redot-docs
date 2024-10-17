github\_url  
hide

# CameraFeed

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

A camera feed gives you access to a single physical camera attached to
your device.

classref-introduction-group

## Description

A camera feed gives you access to a single physical camera attached to
your device. When enabled, Godot will start capturing frames from the
camera which can then be used. See also
`CameraServer<class_CameraServer>`.

\*\*Note:\*\* Many cameras will return YCbCr images which are split into
two textures and need to be combined in a shader. Godot does this
automatically for you if you set the environment to show the camera
image in the background.

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

**format\_changed**() `🔗<class_CameraFeed_signal_format_changed>`

Emitted when the format has changed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**frame\_changed**() `🔗<class_CameraFeed_signal_frame_changed>`

Emitted when a new frame is available.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FeedDataType**: `🔗<enum_CameraFeed_FeedDataType>`

classref-enumeration-constant

`FeedDataType<enum_CameraFeed_FeedDataType>` **FEED\_NOIMAGE** = `0`

No image set for the feed.

classref-enumeration-constant

`FeedDataType<enum_CameraFeed_FeedDataType>` **FEED\_RGB** = `1`

Feed supplies RGB images.

classref-enumeration-constant

`FeedDataType<enum_CameraFeed_FeedDataType>` **FEED\_YCBCR** = `2`

Feed supplies YCbCr images that need to be converted to RGB.

classref-enumeration-constant

`FeedDataType<enum_CameraFeed_FeedDataType>` **FEED\_YCBCR\_SEP** = `3`

Feed supplies separate Y and CbCr images that need to be combined and
converted to RGB.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FeedPosition**: `🔗<enum_CameraFeed_FeedPosition>`

classref-enumeration-constant

`FeedPosition<enum_CameraFeed_FeedPosition>` **FEED\_UNSPECIFIED** = `0`

Unspecified position.

classref-enumeration-constant

`FeedPosition<enum_CameraFeed_FeedPosition>` **FEED\_FRONT** = `1`

Camera is mounted at the front of the device.

classref-enumeration-constant

`FeedPosition<enum_CameraFeed_FeedPosition>` **FEED\_BACK** = `2`

Camera is mounted at the back of the device.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **feed\_is\_active** = `false`
`🔗<class_CameraFeed_property_feed_is_active>`

classref-property-setget

-   `void (No return value.)` **set\_active**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_active**()

If `true`, the feed is active.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **feed\_transform** =
`Transform2D(1, 0, 0, -1, 0, 1)`
`🔗<class_CameraFeed_property_feed_transform>`

classref-property-setget

-   `void (No return value.)` **set\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_transform**()

The transform applied to the camera's image.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **formats** = `[]`
`🔗<class_CameraFeed_property_formats>`

classref-property-setget

-   `Array<class_Array>` **get\_formats**()

Formats supported by the feed. Each entry is a
`Dictionary<class_Dictionary>` describing format parameters.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`FeedDataType<enum_CameraFeed_FeedDataType>` **get\_datatype**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CameraFeed_method_get_datatype>`

Returns feed image data type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CameraFeed_method_get_id>`

Returns the unique ID for this feed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CameraFeed_method_get_name>`

Returns the camera's name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FeedPosition<enum_CameraFeed_FeedPosition>` **get\_position**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CameraFeed_method_get_position>`

Returns the position of camera on the device.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **set\_format**(index: `int<class_int>`, parameters:
`Dictionary<class_Dictionary>`) `🔗<class_CameraFeed_method_set_format>`

Sets the feed format parameters for the given index in the
`formats<class_CameraFeed_property_formats>` array. Returns `true` on
success. By default YUYV encoded stream is transformed to FEED\_RGB.
YUYV encoded stream output format can be changed with
`parameters`.output value:

`separate` will result in FEED\_YCBCR\_SEP

`grayscale` will result in desaturated FEED\_RGB

`copy` will result in FEED\_YCBCR

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_name**(name: `String<class_String>`)
`🔗<class_CameraFeed_method_set_name>`

Sets the camera's name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_position**(position:
`FeedPosition<enum_CameraFeed_FeedPosition>`)
`🔗<class_CameraFeed_method_set_position>`

Sets the position of this camera.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_rgb\_image**(rgb\_image:
`Image<class_Image>`) `🔗<class_CameraFeed_method_set_rgb_image>`

Sets RGB image for this feed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_ycbcr\_image**(ycbcr\_image:
`Image<class_Image>`) `🔗<class_CameraFeed_method_set_ycbcr_image>`

Sets YCbCr image for this feed.
