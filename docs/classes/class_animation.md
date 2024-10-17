github\_url  
hide

# Animation

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Holds data that can be used to animate anything in the engine.

classref-introduction-group

## Description

This resource holds data that can be used to animate anything in the
engine. Animations are divided into tracks and each track must be linked
to a node. The state of that node can be changed through time, by adding
timed keys (events) to the track.

gdscript

\# This creates an animation that makes the node "Enemy" move to the
right by \# 100 pixels in 2.0 seconds. var animation = Animation.new()
var track\_index = animation.add\_track(Animation.TYPE\_VALUE)
animation.track\_set\_path(track\_index, "Enemy:position:x")
animation.track\_insert\_key(track\_index, 0.0, 0)
animation.track\_insert\_key(track\_index, 2.0, 100) animation.length =
2.0

csharp

// This creates an animation that makes the node "Enemy" move to the
right by // 100 pixels in 2.0 seconds. var animation = new Animation();
int trackIndex = animation.AddTrack(Animation.TrackType.Value);
animation.TrackSetPath(trackIndex, "Enemy:position:x");
animation.TrackInsertKey(trackIndex, 0.0f, 0);
animation.TrackInsertKey(trackIndex, 2.0f, 100); animation.Length =
2.0f;

Animations are just data containers, and must be added to nodes such as
an `AnimationPlayer<class_AnimationPlayer>` to be played back. Animation
tracks have different types, each with its own set of dedicated methods.
Check `TrackType<enum_Animation_TrackType>` to see available types.

\*\*Note:\*\* For 3D position/rotation/scale, using the dedicated
`TYPE_POSITION_3D<class_Animation_constant_TYPE_POSITION_3D>`,
`TYPE_ROTATION_3D<class_Animation_constant_TYPE_ROTATION_3D>` and
`TYPE_SCALE_3D<class_Animation_constant_TYPE_SCALE_3D>` track types
instead of `TYPE_VALUE<class_Animation_constant_TYPE_VALUE>` is
recommended for performance reasons.

classref-introduction-group

## Tutorials

-   `Animation documentation index <../tutorials/animation/index>`

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

## Enumerations

classref-enumeration

enum **TrackType**: `🔗<enum_Animation_TrackType>`

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_VALUE** = `0`

Value tracks set values in node properties, but only those which can be
interpolated. For 3D position/rotation/scale, using the dedicated
`TYPE_POSITION_3D<class_Animation_constant_TYPE_POSITION_3D>`,
`TYPE_ROTATION_3D<class_Animation_constant_TYPE_ROTATION_3D>` and
`TYPE_SCALE_3D<class_Animation_constant_TYPE_SCALE_3D>` track types
instead of `TYPE_VALUE<class_Animation_constant_TYPE_VALUE>` is
recommended for performance reasons.

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_POSITION\_3D** = `1`

3D position track (values are stored in `Vector3<class_Vector3>`s).

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_ROTATION\_3D** = `2`

3D rotation track (values are stored in
`Quaternion<class_Quaternion>`s).

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_SCALE\_3D** = `3`

3D scale track (values are stored in `Vector3<class_Vector3>`s).

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_BLEND\_SHAPE** = `4`

Blend shape track.

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_METHOD** = `5`

Method tracks call functions with given arguments per key.

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_BEZIER** = `6`

Bezier tracks are used to interpolate a value using custom curves. They
can also be used to animate sub-properties of vectors and colors (e.g.
alpha value of a `Color<class_Color>`).

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_AUDIO** = `7`

Audio tracks are used to play an audio stream with either type of
`AudioStreamPlayer<class_AudioStreamPlayer>`. The stream can be trimmed
and previewed in the animation.

classref-enumeration-constant

`TrackType<enum_Animation_TrackType>` **TYPE\_ANIMATION** = `8`

Animation tracks play animations in other
`AnimationPlayer<class_AnimationPlayer>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **InterpolationType**: `🔗<enum_Animation_InterpolationType>`

classref-enumeration-constant

`InterpolationType<enum_Animation_InterpolationType>`
**INTERPOLATION\_NEAREST** = `0`

No interpolation (nearest value).

classref-enumeration-constant

`InterpolationType<enum_Animation_InterpolationType>`
**INTERPOLATION\_LINEAR** = `1`

Linear interpolation.

classref-enumeration-constant

`InterpolationType<enum_Animation_InterpolationType>`
**INTERPOLATION\_CUBIC** = `2`

Cubic interpolation. This looks smoother than linear interpolation, but
is more expensive to interpolate. Stick to
`INTERPOLATION_LINEAR<class_Animation_constant_INTERPOLATION_LINEAR>`
for complex 3D animations imported from external software, even if it
requires using a higher animation framerate in return.

classref-enumeration-constant

`InterpolationType<enum_Animation_InterpolationType>`
**INTERPOLATION\_LINEAR\_ANGLE** = `3`

Linear interpolation with shortest path rotation.

\*\*Note:\*\* The result value is always normalized and may not match
the key value.

classref-enumeration-constant

`InterpolationType<enum_Animation_InterpolationType>`
**INTERPOLATION\_CUBIC\_ANGLE** = `4`

Cubic interpolation with shortest path rotation.

\*\*Note:\*\* The result value is always normalized and may not match
the key value.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **UpdateMode**: `🔗<enum_Animation_UpdateMode>`

classref-enumeration-constant

`UpdateMode<enum_Animation_UpdateMode>` **UPDATE\_CONTINUOUS** = `0`

Update between keyframes and hold the value.

classref-enumeration-constant

`UpdateMode<enum_Animation_UpdateMode>` **UPDATE\_DISCRETE** = `1`

Update at the keyframes.

classref-enumeration-constant

`UpdateMode<enum_Animation_UpdateMode>` **UPDATE\_CAPTURE** = `2`

Same as `UPDATE_CONTINUOUS<class_Animation_constant_UPDATE_CONTINUOUS>`
but works as a flag to capture the value of the current object and
perform interpolation in some methods. See also
`AnimationMixer.capture<class_AnimationMixer_method_capture>`,
`AnimationPlayer.playback_auto_capture<class_AnimationPlayer_property_playback_auto_capture>`,
and
`AnimationPlayer.play_with_capture<class_AnimationPlayer_method_play_with_capture>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LoopMode**: `🔗<enum_Animation_LoopMode>`

classref-enumeration-constant

`LoopMode<enum_Animation_LoopMode>` **LOOP\_NONE** = `0`

At both ends of the animation, the animation will stop playing.

classref-enumeration-constant

`LoopMode<enum_Animation_LoopMode>` **LOOP\_LINEAR** = `1`

At both ends of the animation, the animation will be repeated without
changing the playback direction.

classref-enumeration-constant

`LoopMode<enum_Animation_LoopMode>` **LOOP\_PINGPONG** = `2`

Repeats playback and reverse playback at both ends of the animation.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LoopedFlag**: `🔗<enum_Animation_LoopedFlag>`

classref-enumeration-constant

`LoopedFlag<enum_Animation_LoopedFlag>` **LOOPED\_FLAG\_NONE** = `0`

This flag indicates that the animation proceeds without any looping.

classref-enumeration-constant

`LoopedFlag<enum_Animation_LoopedFlag>` **LOOPED\_FLAG\_END** = `1`

This flag indicates that the animation has reached the end of the
animation and just after loop processed.

classref-enumeration-constant

`LoopedFlag<enum_Animation_LoopedFlag>` **LOOPED\_FLAG\_START** = `2`

This flag indicates that the animation has reached the start of the
animation and just after loop processed.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FindMode**: `🔗<enum_Animation_FindMode>`

classref-enumeration-constant

`FindMode<enum_Animation_FindMode>` **FIND\_MODE\_NEAREST** = `0`

Finds the nearest time key.

classref-enumeration-constant

`FindMode<enum_Animation_FindMode>` **FIND\_MODE\_APPROX** = `1`

Finds only the key with approximating the time.

classref-enumeration-constant

`FindMode<enum_Animation_FindMode>` **FIND\_MODE\_EXACT** = `2`

Finds only the key with matching the time.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **capture\_included** = `false`
`🔗<class_Animation_property_capture_included>`

classref-property-setget

-   `bool<class_bool>` **is\_capture\_included**()

Returns `true` if the capture track is included. This is a cached
readonly value for performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **length** = `1.0`
`🔗<class_Animation_property_length>`

classref-property-setget

-   `void (No return value.)` **set\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_length**()

The total length of the animation (in seconds).

\*\*Note:\*\* Length is not delimited by the last key, as this one may
be before or after the end to ensure correct interpolation and looping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`LoopMode<enum_Animation_LoopMode>` **loop\_mode** = `0`
`🔗<class_Animation_property_loop_mode>`

classref-property-setget

-   `void (No return value.)` **set\_loop\_mode**(value:
    `LoopMode<enum_Animation_LoopMode>`)
-   `LoopMode<enum_Animation_LoopMode>` **get\_loop\_mode**()

Determines the behavior of both ends of the animation timeline during
animation playback. This is used for correct interpolation of animation
cycles, and for hinting the player that it must restart the animation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **step** = `0.0333333`
`🔗<class_Animation_property_step>`

classref-property-setget

-   `void (No return value.)` **set\_step**(value: `float<class_float>`)
-   `float<class_float>` **get\_step**()

The animation step value.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_marker**(name:
`StringName<class_StringName>`, time: `float<class_float>`)
`🔗<class_Animation_method_add_marker>`

Adds a marker to this Animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **add\_track**(type:
`TrackType<enum_Animation_TrackType>`, at\_position: `int<class_int>` =
-1) `🔗<class_Animation_method_add_track>`

Adds a track to the Animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>`
**animation\_track\_get\_key\_animation**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_animation_track_get_key_animation>`

Returns the animation name at the key identified by `key_idx`. The
`track_idx` must be the index of an Animation Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **animation\_track\_insert\_key**(track\_idx:
`int<class_int>`, time: `float<class_float>`, animation:
`StringName<class_StringName>`)
`🔗<class_Animation_method_animation_track_insert_key>`

Inserts a key with value `animation` at the given `time` (in seconds).
The `track_idx` must be the index of an Animation Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**animation\_track\_set\_key\_animation**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`, animation: `StringName<class_StringName>`)
`🔗<class_Animation_method_animation_track_set_key_animation>`

Sets the key identified by `key_idx` to value `animation`. The
`track_idx` must be the index of an Animation Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **audio\_track\_get\_key\_end\_offset**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_audio_track_get_key_end_offset>`

Returns the end offset of the key identified by `key_idx`. The
`track_idx` must be the index of an Audio Track.

End offset is the number of seconds cut off at the ending of the audio
stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**audio\_track\_get\_key\_start\_offset**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_audio_track_get_key_start_offset>`

Returns the start offset of the key identified by `key_idx`. The
`track_idx` must be the index of an Audio Track.

Start offset is the number of seconds cut off at the beginning of the
audio stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Resource<class_Resource>`
**audio\_track\_get\_key\_stream**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_audio_track_get_key_stream>`

Returns the audio stream of the key identified by `key_idx`. The
`track_idx` must be the index of an Audio Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **audio\_track\_insert\_key**(track\_idx:
`int<class_int>`, time: `float<class_float>`, stream:
`Resource<class_Resource>`, start\_offset: `float<class_float>` = 0,
end\_offset: `float<class_float>` = 0)
`🔗<class_Animation_method_audio_track_insert_key>`

Inserts an Audio Track key at the given `time` in seconds. The
`track_idx` must be the index of an Audio Track.

`stream` is the `AudioStream<class_AudioStream>` resource to play.
`start_offset` is the number of seconds cut off at the beginning of the
audio stream, while `end_offset` is at the ending.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **audio\_track\_is\_use\_blend**(track\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_audio_track_is_use_blend>`

Returns `true` if the track at `track_idx` will be blended with other
animations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**audio\_track\_set\_key\_end\_offset**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`, offset: `float<class_float>`)
`🔗<class_Animation_method_audio_track_set_key_end_offset>`

Sets the end offset of the key identified by `key_idx` to value
`offset`. The `track_idx` must be the index of an Audio Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**audio\_track\_set\_key\_start\_offset**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`, offset: `float<class_float>`)
`🔗<class_Animation_method_audio_track_set_key_start_offset>`

Sets the start offset of the key identified by `key_idx` to value
`offset`. The `track_idx` must be the index of an Audio Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **audio\_track\_set\_key\_stream**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`, stream:
`Resource<class_Resource>`)
`🔗<class_Animation_method_audio_track_set_key_stream>`

Sets the stream of the key identified by `key_idx` to value `stream`.
The `track_idx` must be the index of an Audio Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **audio\_track\_set\_use\_blend**(track\_idx:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_Animation_method_audio_track_set_use_blend>`

Sets whether the track will be blended with other animations. If `true`,
the audio playback volume changes depending on the blend value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**bezier\_track\_get\_key\_in\_handle**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_bezier_track_get_key_in_handle>`

Returns the in handle of the key identified by `key_idx`. The
`track_idx` must be the index of a Bezier Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**bezier\_track\_get\_key\_out\_handle**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_bezier_track_get_key_out_handle>`

Returns the out handle of the key identified by `key_idx`. The
`track_idx` must be the index of a Bezier Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **bezier\_track\_get\_key\_value**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_bezier_track_get_key_value>`

Returns the value of the key identified by `key_idx`. The `track_idx`
must be the index of a Bezier Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **bezier\_track\_insert\_key**(track\_idx:
`int<class_int>`, time: `float<class_float>`, value:
`float<class_float>`, in\_handle: `Vector2<class_Vector2>` = Vector2(0,
0), out\_handle: `Vector2<class_Vector2>` = Vector2(0, 0))
`🔗<class_Animation_method_bezier_track_insert_key>`

Inserts a Bezier Track key at the given `time` in seconds. The
`track_idx` must be the index of a Bezier Track.

`in_handle` is the left-side weight of the added Bezier curve point,
`out_handle` is the right-side one, while `value` is the actual value at
this point.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **bezier\_track\_interpolate**(track\_idx:
`int<class_int>`, time: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_bezier_track_interpolate>`

Returns the interpolated value at the given `time` (in seconds). The
`track_idx` must be the index of a Bezier Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**bezier\_track\_set\_key\_in\_handle**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`, in\_handle: `Vector2<class_Vector2>`,
balanced\_value\_time\_ratio: `float<class_float>` = 1.0)
`🔗<class_Animation_method_bezier_track_set_key_in_handle>`

Sets the in handle of the key identified by `key_idx` to value
`in_handle`. The `track_idx` must be the index of a Bezier Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**bezier\_track\_set\_key\_out\_handle**(track\_idx: `int<class_int>`,
key\_idx: `int<class_int>`, out\_handle: `Vector2<class_Vector2>`,
balanced\_value\_time\_ratio: `float<class_float>` = 1.0)
`🔗<class_Animation_method_bezier_track_set_key_out_handle>`

Sets the out handle of the key identified by `key_idx` to value
`out_handle`. The `track_idx` must be the index of a Bezier Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **bezier\_track\_set\_key\_value**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`, value:
`float<class_float>`)
`🔗<class_Animation_method_bezier_track_set_key_value>`

Sets the value of the key identified by `key_idx` to the given value.
The `track_idx` must be the index of a Bezier Track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **blend\_shape\_track\_insert\_key**(track\_idx:
`int<class_int>`, time: `float<class_float>`, amount:
`float<class_float>`)
`🔗<class_Animation_method_blend_shape_track_insert_key>`

Inserts a key in a given blend shape track. Returns the key index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **blend\_shape\_track\_interpolate**(track\_idx:
`int<class_int>`, time\_sec: `float<class_float>`, backward:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_blend_shape_track_interpolate>`

Returns the interpolated blend shape value at the given time (in
seconds). The `track_idx` must be the index of a blend shape track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**() `🔗<class_Animation_method_clear>`

Clear the animation (clear all tracks and reset all).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **compress**(page\_size: `int<class_int>` =
8192, fps: `int<class_int>` = 120, split\_tolerance:
`float<class_float>` = 4.0) `🔗<class_Animation_method_compress>`

Compress the animation and all its tracks in-place. This will make
`track_is_compressed<class_Animation_method_track_is_compressed>` return
`true` once called on this **Animation**. Compressed tracks require less
memory to be played, and are designed to be used for complex 3D
animations (such as cutscenes) imported from external 3D software.
Compression is lossy, but the difference is usually not noticeable in
real world conditions.

\*\*Note:\*\* Compressed tracks have various limitations (such as not
being editable from the editor), so only use compressed animations if
you actually need them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **copy\_track**(track\_idx: `int<class_int>`,
to\_animation: `Animation<class_Animation>`)
`🔗<class_Animation_method_copy_track>`

Adds a new track to `to_animation` that is a copy of the given track
from this animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **find\_track**(path: `NodePath<class_NodePath>`, type:
`TrackType<enum_Animation_TrackType>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_find_track>`

Returns the index of the specified track. If the track is not found,
return -1.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_marker\_at\_time**(time:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_get_marker_at_time>`

Returns the name of the marker located at the given time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_marker\_color**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_get_marker_color>`

Returns the given marker's color.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_marker\_names**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_get_marker_names>`

Returns every marker in this Animation, sorted ascending by time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_marker\_time**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_get_marker_time>`

Returns the given marker's time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_next\_marker**(time:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_get_next_marker>`

Returns the closest marker that comes after the given time. If no such
marker exists, an empty string is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_prev\_marker**(time:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_get_prev_marker>`

Returns the closest marker that comes before the given time. If no such
marker exists, an empty string is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_track\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_get_track_count>`

Returns the amount of tracks in the animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_marker**(name: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_has_marker>`

Returns `true` if this Animation contains a marker with the given name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **method\_track\_get\_name**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_method_track_get_name>`

Returns the method name of a method track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **method\_track\_get\_params**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_method_track_get_params>`

Returns the arguments values to be called on a method track for a given
key in a given track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **optimize**(allowed\_velocity\_err:
`float<class_float>` = 0.01, allowed\_angular\_err: `float<class_float>`
= 0.01, precision: `int<class_int>` = 3)
`🔗<class_Animation_method_optimize>`

Optimize the animation and all its tracks in-place. This will preserve
only as many keys as are necessary to keep the animation within the
specified bounds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **position\_track\_insert\_key**(track\_idx:
`int<class_int>`, time: `float<class_float>`, position:
`Vector3<class_Vector3>`)
`🔗<class_Animation_method_position_track_insert_key>`

Inserts a key in a given 3D position track. Returns the key index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **position\_track\_interpolate**(track\_idx:
`int<class_int>`, time\_sec: `float<class_float>`, backward:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_position_track_interpolate>`

Returns the interpolated position value at the given time (in seconds).
The `track_idx` must be the index of a 3D position track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_marker**(name:
`StringName<class_StringName>`)
`🔗<class_Animation_method_remove_marker>`

Removes the marker with the given name from this Animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_track**(track\_idx:
`int<class_int>`) `🔗<class_Animation_method_remove_track>`

Removes a track by specifying the track index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **rotation\_track\_insert\_key**(track\_idx:
`int<class_int>`, time: `float<class_float>`, rotation:
`Quaternion<class_Quaternion>`)
`🔗<class_Animation_method_rotation_track_insert_key>`

Inserts a key in a given 3D rotation track. Returns the key index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Quaternion<class_Quaternion>`
**rotation\_track\_interpolate**(track\_idx: `int<class_int>`,
time\_sec: `float<class_float>`, backward: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_rotation_track_interpolate>`

Returns the interpolated rotation value at the given time (in seconds).
The `track_idx` must be the index of a 3D rotation track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **scale\_track\_insert\_key**(track\_idx:
`int<class_int>`, time: `float<class_float>`, scale:
`Vector3<class_Vector3>`)
`🔗<class_Animation_method_scale_track_insert_key>`

Inserts a key in a given 3D scale track. Returns the key index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **scale\_track\_interpolate**(track\_idx:
`int<class_int>`, time\_sec: `float<class_float>`, backward:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_scale_track_interpolate>`

Returns the interpolated scale value at the given time (in seconds). The
`track_idx` must be the index of a 3D scale track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_marker\_color**(name:
`StringName<class_StringName>`, color: `Color<class_Color>`)
`🔗<class_Animation_method_set_marker_color>`

Sets the given marker's color.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **track\_find\_key**(track\_idx: `int<class_int>`,
time: `float<class_float>`, find\_mode:
`FindMode<enum_Animation_FindMode>` = 0, limit: `bool<class_bool>` =
false, backward: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_find_key>`

Finds the key index by time in a given track. Optionally, only find it
if the approx/exact time is given.

If `limit` is `true`, it does not return keys outside the animation
range.

If `backward` is `true`, the direction is reversed in methods that rely
on one directional processing.

For example, in case `find_mode` is
`FIND_MODE_NEAREST<class_Animation_constant_FIND_MODE_NEAREST>`, if
there is no key in the current position just after seeked, the first key
found is retrieved by searching before the position, but if `backward`
is `true`, the first key found is retrieved after the position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **track\_get\_interpolation\_loop\_wrap**(track\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_get_interpolation_loop_wrap>`

Returns `true` if the track at `track_idx` wraps the interpolation loop.
New tracks wrap the interpolation loop by default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`InterpolationType<enum_Animation_InterpolationType>`
**track\_get\_interpolation\_type**(track\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_get_interpolation_type>`

Returns the interpolation type of a given track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **track\_get\_key\_count**(track\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_get_key_count>`

Returns the number of keys in a given track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **track\_get\_key\_time**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_get_key_time>`

Returns the time at which the key is located.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **track\_get\_key\_transition**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_get_key_transition>`

Returns the transition curve (easing) for a specific key (see the
built-in math function
`@GlobalScope.ease<class_@GlobalScope_method_ease>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **track\_get\_key\_value**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_get_key_value>`

Returns the value of a given key in a given track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **track\_get\_path**(track\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_get_path>`

Gets the path of a track. For more information on the path format, see
`track_set_path<class_Animation_method_track_set_path>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TrackType<enum_Animation_TrackType>` **track\_get\_type**(track\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_get_type>`

Gets the type of a track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **track\_insert\_key**(track\_idx: `int<class_int>`,
time: `float<class_float>`, key: `Variant<class_Variant>`, transition:
`float<class_float>` = 1) `🔗<class_Animation_method_track_insert_key>`

Inserts a generic key in a given track. Returns the key index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **track\_is\_compressed**(track\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_is_compressed>`

Returns `true` if the track is compressed, `false` otherwise. See also
`compress<class_Animation_method_compress>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **track\_is\_enabled**(track\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_is_enabled>`

Returns `true` if the track at index `track_idx` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **track\_is\_imported**(track\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_track_is_imported>`

Returns `true` if the given track is imported. Else, return `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_move\_down**(track\_idx:
`int<class_int>`) `🔗<class_Animation_method_track_move_down>`

Moves a track down.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_move\_to**(track\_idx:
`int<class_int>`, to\_idx: `int<class_int>`)
`🔗<class_Animation_method_track_move_to>`

Changes the index position of track `track_idx` to the one defined in
`to_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_move\_up**(track\_idx:
`int<class_int>`) `🔗<class_Animation_method_track_move_up>`

Moves a track up.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_remove\_key**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`)
`🔗<class_Animation_method_track_remove_key>`

Removes a key by index in a given track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_remove\_key\_at\_time**(track\_idx:
`int<class_int>`, time: `float<class_float>`)
`🔗<class_Animation_method_track_remove_key_at_time>`

Removes a key at `time` in a given track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_set\_enabled**(track\_idx:
`int<class_int>`, enabled: `bool<class_bool>`)
`🔗<class_Animation_method_track_set_enabled>`

Enables/disables the given track. Tracks are enabled by default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_set\_imported**(track\_idx:
`int<class_int>`, imported: `bool<class_bool>`)
`🔗<class_Animation_method_track_set_imported>`

Sets the given track as imported or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**track\_set\_interpolation\_loop\_wrap**(track\_idx: `int<class_int>`,
interpolation: `bool<class_bool>`)
`🔗<class_Animation_method_track_set_interpolation_loop_wrap>`

If `true`, the track at `track_idx` wraps the interpolation loop.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**track\_set\_interpolation\_type**(track\_idx: `int<class_int>`,
interpolation: `InterpolationType<enum_Animation_InterpolationType>`)
`🔗<class_Animation_method_track_set_interpolation_type>`

Sets the interpolation type of a given track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_set\_key\_time**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`, time:
`float<class_float>`) `🔗<class_Animation_method_track_set_key_time>`

Sets the time of an existing key.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_set\_key\_transition**(track\_idx:
`int<class_int>`, key\_idx: `int<class_int>`, transition:
`float<class_float>`)
`🔗<class_Animation_method_track_set_key_transition>`

Sets the transition curve (easing) for a specific key (see the built-in
math function `@GlobalScope.ease<class_@GlobalScope_method_ease>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_set\_key\_value**(track\_idx:
`int<class_int>`, key: `int<class_int>`, value:
`Variant<class_Variant>`)
`🔗<class_Animation_method_track_set_key_value>`

Sets the value of an existing key.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_set\_path**(track\_idx:
`int<class_int>`, path: `NodePath<class_NodePath>`)
`🔗<class_Animation_method_track_set_path>`

Sets the path of a track. Paths must be valid scene-tree paths to a node
and must be specified starting from the
`AnimationMixer.root_node<class_AnimationMixer_property_root_node>` that
will reproduce the animation. Tracks that control properties or bones
must append their name after the path, separated by `":"`.

For example, `"character/skeleton:ankle"` or
`"character/mesh:transform/local"`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **track\_swap**(track\_idx: `int<class_int>`,
with\_idx: `int<class_int>`) `🔗<class_Animation_method_track_swap>`

Swaps the track `track_idx`'s index position with the track `with_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`UpdateMode<enum_Animation_UpdateMode>`
**value\_track\_get\_update\_mode**(track\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_value_track_get_update_mode>`

Returns the update mode of a value track.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **value\_track\_interpolate**(track\_idx:
`int<class_int>`, time\_sec: `float<class_float>`, backward:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Animation_method_value_track_interpolate>`

Returns the interpolated value at the given time (in seconds). The
`track_idx` must be the index of a value track.

A `backward` mainly affects the direction of key retrieval of the track
with `UPDATE_DISCRETE<class_Animation_constant_UPDATE_DISCRETE>`
converted by
`AnimationMixer.ANIMATION_CALLBACK_MODE_DISCRETE_FORCE_CONTINUOUS<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_DISCRETE_FORCE_CONTINUOUS>`
to match the result with
`track_find_key<class_Animation_method_track_find_key>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**value\_track\_set\_update\_mode**(track\_idx: `int<class_int>`, mode:
`UpdateMode<enum_Animation_UpdateMode>`)
`🔗<class_Animation_method_value_track_set_update_mode>`

Sets the update mode (see `UpdateMode<enum_Animation_UpdateMode>`) of a
value track.
