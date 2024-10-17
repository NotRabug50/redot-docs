github\_url  
hide

# SpriteFrames

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Sprite frame library for AnimatedSprite2D and AnimatedSprite3D.

classref-introduction-group

## Description

Sprite frame library for an `AnimatedSprite2D<class_AnimatedSprite2D>`
or `AnimatedSprite3D<class_AnimatedSprite3D>` node. Contains frames and
animation data for playback.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_animation**(anim:
`StringName<class_StringName>`)
`🔗<class_SpriteFrames_method_add_animation>`

Adds a new `anim` animation to the library.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_frame**(anim:
`StringName<class_StringName>`, texture: `Texture2D<class_Texture2D>`,
duration: `float<class_float>` = 1.0, at\_position: `int<class_int>` =
-1) `🔗<class_SpriteFrames_method_add_frame>`

Adds a frame to the `anim` animation. If `at_position` is `-1`, the
frame will be added to the end of the animation. `duration` specifies
the relative duration, see
`get_frame_duration<class_SpriteFrames_method_get_frame_duration>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**(anim:
`StringName<class_StringName>`) `🔗<class_SpriteFrames_method_clear>`

Removes all frames from the `anim` animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_all**()
`🔗<class_SpriteFrames_method_clear_all>`

Removes all animations. An empty `default` animation will be created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **duplicate\_animation**(anim\_from:
`StringName<class_StringName>`, anim\_to:
`StringName<class_StringName>`)
`🔗<class_SpriteFrames_method_duplicate_animation>`

Duplicates the animation `anim_from` to a new animation named `anim_to`.
Fails if `anim_to` already exists, or if `anim_from` does not exist.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_animation\_loop**(anim:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteFrames_method_get_animation_loop>`

Returns `true` if the given animation is configured to loop when it
finishes playing. Otherwise, returns `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_animation\_names**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteFrames_method_get_animation_names>`

Returns an array containing the names associated to each animation.
Values are placed in alphabetical order.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_animation\_speed**(anim:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteFrames_method_get_animation_speed>`

Returns the speed in frames per second for the `anim` animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_frame\_count**(anim:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteFrames_method_get_frame_count>`

Returns the number of frames for the `anim` animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_frame\_duration**(anim:
`StringName<class_StringName>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteFrames_method_get_frame_duration>`

Returns a relative duration of the frame `idx` in the `anim` animation
(defaults to `1.0`). For example, a frame with a duration of `2.0` is
displayed twice as long as a frame with a duration of `1.0`. You can
calculate the absolute duration (in seconds) of a frame using the
following formula:

    absolute_duration = relative_duration / (animation_fps * abs(playing_speed))

In this example, `playing_speed` refers to either
`AnimatedSprite2D.get_playing_speed<class_AnimatedSprite2D_method_get_playing_speed>`
or
`AnimatedSprite3D.get_playing_speed<class_AnimatedSprite3D_method_get_playing_speed>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_frame\_texture**(anim:
`StringName<class_StringName>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteFrames_method_get_frame_texture>`

Returns the texture of the frame `idx` in the `anim` animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_animation**(anim:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteFrames_method_has_animation>`

Returns `true` if the `anim` animation exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_animation**(anim:
`StringName<class_StringName>`)
`🔗<class_SpriteFrames_method_remove_animation>`

Removes the `anim` animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_frame**(anim:
`StringName<class_StringName>`, idx: `int<class_int>`)
`🔗<class_SpriteFrames_method_remove_frame>`

Removes the `anim` animation's frame `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rename\_animation**(anim:
`StringName<class_StringName>`, newname: `StringName<class_StringName>`)
`🔗<class_SpriteFrames_method_rename_animation>`

Changes the `anim` animation's name to `newname`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_animation\_loop**(anim:
`StringName<class_StringName>`, loop: `bool<class_bool>`)
`🔗<class_SpriteFrames_method_set_animation_loop>`

If `loop` is `true`, the `anim` animation will loop when it reaches the
end, or the start if it is played in reverse.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_animation\_speed**(anim:
`StringName<class_StringName>`, fps: `float<class_float>`)
`🔗<class_SpriteFrames_method_set_animation_speed>`

Sets the speed for the `anim` animation in frames per second.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_frame**(anim:
`StringName<class_StringName>`, idx: `int<class_int>`, texture:
`Texture2D<class_Texture2D>`, duration: `float<class_float>` = 1.0)
`🔗<class_SpriteFrames_method_set_frame>`

Sets the `texture` and the `duration` of the frame `idx` in the `anim`
animation. `duration` specifies the relative duration, see
`get_frame_duration<class_SpriteFrames_method_get_frame_duration>` for
details.
