github\_url  
hide

# CameraServer

**Inherits:** `Object<class_Object>`

Server keeping track of different cameras accessible in Godot.

classref-introduction-group

## Description

The **CameraServer** keeps track of different cameras accessible in
Godot. These are external cameras such as webcams or the cameras on your
phone.

It is notably used to provide AR modules with a video feed from the
camera.

\*\*Note:\*\* This class is currently only implemented on Linux, macOS,
and iOS, on other platforms no `CameraFeed<class_CameraFeed>`s will be
available. To get a `CameraFeed<class_CameraFeed>` on iOS, the camera
plugin from
[godot-ios-plugins](https://github.com/godotengine/godot-ios-plugins) is
required.

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

**camera\_feed\_added**(id: `int<class_int>`)
`🔗<class_CameraServer_signal_camera_feed_added>`

Emitted when a `CameraFeed<class_CameraFeed>` is added (e.g. a webcam is
plugged in).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**camera\_feed\_removed**(id: `int<class_int>`)
`🔗<class_CameraServer_signal_camera_feed_removed>`

Emitted when a `CameraFeed<class_CameraFeed>` is removed (e.g. a webcam
is unplugged).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FeedImage**: `🔗<enum_CameraServer_FeedImage>`

classref-enumeration-constant

`FeedImage<enum_CameraServer_FeedImage>` **FEED\_RGBA\_IMAGE** = `0`

The RGBA camera image.

classref-enumeration-constant

`FeedImage<enum_CameraServer_FeedImage>` **FEED\_YCBCR\_IMAGE** = `0`

The [YCbCr](https://en.wikipedia.org/wiki/YCbCr) camera image.

classref-enumeration-constant

`FeedImage<enum_CameraServer_FeedImage>` **FEED\_Y\_IMAGE** = `0`

The Y component camera image.

classref-enumeration-constant

`FeedImage<enum_CameraServer_FeedImage>` **FEED\_CBCR\_IMAGE** = `1`

The CbCr component camera image.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_feed**(feed:
`CameraFeed<class_CameraFeed>`) `🔗<class_CameraServer_method_add_feed>`

Adds the camera `feed` to the camera server.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`CameraFeed<class_CameraFeed>`\] **feeds**()
`🔗<class_CameraServer_method_feeds>`

Returns an array of `CameraFeed<class_CameraFeed>`s.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CameraFeed<class_CameraFeed>` **get\_feed**(index: `int<class_int>`)
`🔗<class_CameraServer_method_get_feed>`

Returns the `CameraFeed<class_CameraFeed>` corresponding to the camera
with the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_feed\_count**()
`🔗<class_CameraServer_method_get_feed_count>`

Returns the number of `CameraFeed<class_CameraFeed>`s registered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_feed**(feed:
`CameraFeed<class_CameraFeed>`)
`🔗<class_CameraServer_method_remove_feed>`

Removes the specified camera `feed`.
