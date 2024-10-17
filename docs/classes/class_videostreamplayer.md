github\_url  
hide

# VideoStreamPlayer

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A control used for video playback.

classref-introduction-group

## Description

A control used for playback of `VideoStream<class_VideoStream>`
resources.

Supported video formats are [Ogg Theora](https://www.theora.org/)
(`.ogv`, `VideoStreamTheora<class_VideoStreamTheora>`) and any format
exposed via a GDExtension plugin.

\*\*Warning:\*\* On Web, video playback *will* perform poorly due to
missing architecture-specific assembly optimizations.

classref-introduction-group

## Tutorials

-   `Playing videos <../tutorials/animation/playing_videos>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**finished**() `🔗<class_VideoStreamPlayer_signal_finished>`

Emitted when playback is finished.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **audio\_track** = `0`
`🔗<class_VideoStreamPlayer_property_audio_track>`

classref-property-setget

-   `void (No return value.)` **set\_audio\_track**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_audio\_track**()

The embedded audio track to play.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **autoplay** = `false`
`🔗<class_VideoStreamPlayer_property_autoplay>`

classref-property-setget

-   `void (No return value.)` **set\_autoplay**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **has\_autoplay**()

If `true`, playback starts when the scene loads.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **buffering\_msec** = `500`
`🔗<class_VideoStreamPlayer_property_buffering_msec>`

classref-property-setget

-   `void (No return value.)` **set\_buffering\_msec**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_buffering\_msec**()

Amount of time in milliseconds to store in buffer while playing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **bus** = `&"Master"`
`🔗<class_VideoStreamPlayer_property_bus>`

classref-property-setget

-   `void (No return value.)` **set\_bus**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_bus**()

Audio bus to use for sound playback.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **expand** = `false`
`🔗<class_VideoStreamPlayer_property_expand>`

classref-property-setget

-   `void (No return value.)` **set\_expand**(value: `bool<class_bool>`)
-   `bool<class_bool>` **has\_expand**()

If `true`, the video scales to the control size. Otherwise, the control
minimum size will be automatically adjusted to match the video stream's
dimensions.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **loop** = `false`
`🔗<class_VideoStreamPlayer_property_loop>`

classref-property-setget

-   `void (No return value.)` **set\_loop**(value: `bool<class_bool>`)
-   `bool<class_bool>` **has\_loop**()

If `true`, the video restarts when it reaches its end.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **paused** = `false`
`🔗<class_VideoStreamPlayer_property_paused>`

classref-property-setget

-   `void (No return value.)` **set\_paused**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_paused**()

If `true`, the video is paused.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VideoStream<class_VideoStream>` **stream**
`🔗<class_VideoStreamPlayer_property_stream>`

classref-property-setget

-   `void (No return value.)` **set\_stream**(value:
    `VideoStream<class_VideoStream>`)
-   `VideoStream<class_VideoStream>` **get\_stream**()

The assigned video stream. See description for supported formats.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **stream\_position**
`🔗<class_VideoStreamPlayer_property_stream_position>`

classref-property-setget

-   `void (No return value.)` **set\_stream\_position**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_stream\_position**()

The current position of the stream, in seconds.

\*\*Note:\*\* Changing this value won't have any effect as seeking is
not implemented yet, except in video formats implemented by a
GDExtension add-on.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volume**
`🔗<class_VideoStreamPlayer_property_volume>`

classref-property-setget

-   `void (No return value.)` **set\_volume**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volume**()

Audio volume as a linear value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volume\_db** = `0.0`
`🔗<class_VideoStreamPlayer_property_volume_db>`

classref-property-setget

-   `void (No return value.)` **set\_volume\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volume\_db**()

Audio volume in dB.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_stream\_length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VideoStreamPlayer_method_get_stream_length>`

The length of the current stream, in seconds.

\*\*Note:\*\* For `VideoStreamTheora<class_VideoStreamTheora>` streams
(the built-in format supported by Godot), this value will always be
zero, as getting the stream length is not implemented yet. The feature
may be supported by video formats implemented by a GDExtension add-on.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_stream\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VideoStreamPlayer_method_get_stream_name>`

Returns the video stream's name, or `"<No Stream>"` if no video stream
is assigned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_video\_texture**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VideoStreamPlayer_method_get_video_texture>`

Returns the current frame as a `Texture2D<class_Texture2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_playing**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VideoStreamPlayer_method_is_playing>`

Returns `true` if the video is playing.

\*\*Note:\*\* The video is still considered playing if paused during
playback.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play**()
`🔗<class_VideoStreamPlayer_method_play>`

Starts the video playback from the beginning. If the video is paused,
this will not unpause the video.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**()
`🔗<class_VideoStreamPlayer_method_stop>`

Stops the video playback and sets the stream position to 0.

\*\*Note:\*\* Although the stream position will be set to 0, the first
frame of the video stream won't become the current frame.
