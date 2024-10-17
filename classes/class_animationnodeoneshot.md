github\_url  
hide

# AnimationNodeOneShot

**Inherits:** `AnimationNodeSync<class_AnimationNodeSync>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Plays an animation once in an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

classref-introduction-group

## Description

A resource to add to an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`. This animation
node will execute a sub-animation and return once it finishes. Blend
times for fading in and out can be customized, as well as filters.

After setting the request and changing the animation playback, the
one-shot node automatically clears the request on the next process frame
by setting its `request` value to
`ONE_SHOT_REQUEST_NONE<class_AnimationNodeOneShot_constant_ONE_SHOT_REQUEST_NONE>`.

gdscript

\# Play child animation connected to "shot" port.
animation\_tree.set("parameters/OneShot/request",
AnimationNodeOneShot.ONE\_SHOT\_REQUEST\_FIRE) \# Alternative syntax
(same result as above). animation\_tree\["parameters/OneShot/request"\]
= AnimationNodeOneShot.ONE\_SHOT\_REQUEST\_FIRE

\# Abort child animation connected to "shot" port.
animation\_tree.set("parameters/OneShot/request",
AnimationNodeOneShot.ONE\_SHOT\_REQUEST\_ABORT) \# Alternative syntax
(same result as above). animation\_tree\["parameters/OneShot/request"\]
= AnimationNodeOneShot.ONE\_SHOT\_REQUEST\_ABORT

\# Abort child animation with fading out connected to "shot" port.
animation\_tree.set("parameters/OneShot/request",
AnimationNodeOneShot.ONE\_SHOT\_REQUEST\_FADE\_OUT) \# Alternative
syntax (same result as above).
animation\_tree\["parameters/OneShot/request"\] =
AnimationNodeOneShot.ONE\_SHOT\_REQUEST\_FADE\_OUT

\# Get current state (read-only).
animation\_tree.get("parameters/OneShot/active") \# Alternative syntax
(same result as above). animation\_tree\["parameters/OneShot/active"\]

\# Get current internal state (read-only).
animation\_tree.get("parameters/OneShot/internal\_active") \#
Alternative syntax (same result as above).
animation\_tree\["parameters/OneShot/internal\_active"\]

csharp

// Play child animation connected to "shot" port.
animationTree.Set("parameters/OneShot/request",
(int)AnimationNodeOneShot.OneShotRequest.Fire);

// Abort child animation connected to "shot" port.
animationTree.Set("parameters/OneShot/request",
(int)AnimationNodeOneShot.OneShotRequest.Abort);

// Abort child animation with fading out connected to "shot" port.
animationTree.Set("parameters/OneShot/request",
(int)AnimationNodeOneShot.OneShotRequest.FadeOut);

// Get current state (read-only).
animationTree.Get("parameters/OneShot/active");

// Get current internal state (read-only).
animationTree.Get("parameters/OneShot/internal\_active");

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **OneShotRequest**: `🔗<enum_AnimationNodeOneShot_OneShotRequest>`

classref-enumeration-constant

`OneShotRequest<enum_AnimationNodeOneShot_OneShotRequest>`
**ONE\_SHOT\_REQUEST\_NONE** = `0`

The default state of the request. Nothing is done.

classref-enumeration-constant

`OneShotRequest<enum_AnimationNodeOneShot_OneShotRequest>`
**ONE\_SHOT\_REQUEST\_FIRE** = `1`

The request to play the animation connected to "shot" port.

classref-enumeration-constant

`OneShotRequest<enum_AnimationNodeOneShot_OneShotRequest>`
**ONE\_SHOT\_REQUEST\_ABORT** = `2`

The request to stop the animation connected to "shot" port.

classref-enumeration-constant

`OneShotRequest<enum_AnimationNodeOneShot_OneShotRequest>`
**ONE\_SHOT\_REQUEST\_FADE\_OUT** = `3`

The request to fade out the animation connected to "shot" port.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MixMode**: `🔗<enum_AnimationNodeOneShot_MixMode>`

classref-enumeration-constant

`MixMode<enum_AnimationNodeOneShot_MixMode>` **MIX\_MODE\_BLEND** = `0`

Blends two animations. See also
`AnimationNodeBlend2<class_AnimationNodeBlend2>`.

classref-enumeration-constant

`MixMode<enum_AnimationNodeOneShot_MixMode>` **MIX\_MODE\_ADD** = `1`

Blends two animations additively. See also
`AnimationNodeAdd2<class_AnimationNodeAdd2>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **autorestart** = `false`
`🔗<class_AnimationNodeOneShot_property_autorestart>`

classref-property-setget

-   `void (No return value.)` **set\_autorestart**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **has\_autorestart**()

If `true`, the sub-animation will restart automatically after finishing.

In other words, to start auto restarting, the animation must be played
once with the
`ONE_SHOT_REQUEST_FIRE<class_AnimationNodeOneShot_constant_ONE_SHOT_REQUEST_FIRE>`
request. The
`ONE_SHOT_REQUEST_ABORT<class_AnimationNodeOneShot_constant_ONE_SHOT_REQUEST_ABORT>`
request stops the auto restarting, but it does not disable the
`autorestart<class_AnimationNodeOneShot_property_autorestart>` itself.
So, the
`ONE_SHOT_REQUEST_FIRE<class_AnimationNodeOneShot_constant_ONE_SHOT_REQUEST_FIRE>`
request will start auto restarting again.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **autorestart\_delay** = `1.0`
`🔗<class_AnimationNodeOneShot_property_autorestart_delay>`

classref-property-setget

-   `void (No return value.)` **set\_autorestart\_delay**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_autorestart\_delay**()

The delay after which the automatic restart is triggered, in seconds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **autorestart\_random\_delay** = `0.0`
`🔗<class_AnimationNodeOneShot_property_autorestart_random_delay>`

classref-property-setget

-   `void (No return value.)` **set\_autorestart\_random\_delay**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_autorestart\_random\_delay**()

If `autorestart<class_AnimationNodeOneShot_property_autorestart>` is
`true`, a random additional delay (in seconds) between 0 and this value
will be added to
`autorestart_delay<class_AnimationNodeOneShot_property_autorestart_delay>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **break\_loop\_at\_end** = `false`
`🔗<class_AnimationNodeOneShot_property_break_loop_at_end>`

classref-property-setget

-   `void (No return value.)` **set\_break\_loop\_at\_end**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_loop\_broken\_at\_end**()

If `true`, breaks the loop at the end of the loop cycle for transition,
even if the animation is looping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Curve<class_Curve>` **fadein\_curve**
`🔗<class_AnimationNodeOneShot_property_fadein_curve>`

classref-property-setget

-   `void (No return value.)` **set\_fadein\_curve**(value:
    `Curve<class_Curve>`)
-   `Curve<class_Curve>` **get\_fadein\_curve**()

Determines how cross-fading between animations is eased. If empty, the
transition will be linear.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fadein\_time** = `0.0`
`🔗<class_AnimationNodeOneShot_property_fadein_time>`

classref-property-setget

-   `void (No return value.)` **set\_fadein\_time**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fadein\_time**()

The fade-in duration. For example, setting this to `1.0` for a 5 second
length animation will produce a cross-fade that starts at 0 second and
ends at 1 second during the animation.

\*\*Note:\*\* **AnimationNodeOneShot** transitions the current state
after the end of the fading. When
`AnimationNodeOutput<class_AnimationNodeOutput>` is considered as the
most upstream, so the
`fadein_time<class_AnimationNodeOneShot_property_fadein_time>` is scaled
depending on the downstream delta. For example, if this value is set to
`1.0` and a `AnimationNodeTimeScale<class_AnimationNodeTimeScale>` with
a value of `2.0` is chained downstream, the actual processing time will
be 0.5 second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Curve<class_Curve>` **fadeout\_curve**
`🔗<class_AnimationNodeOneShot_property_fadeout_curve>`

classref-property-setget

-   `void (No return value.)` **set\_fadeout\_curve**(value:
    `Curve<class_Curve>`)
-   `Curve<class_Curve>` **get\_fadeout\_curve**()

Determines how cross-fading between animations is eased. If empty, the
transition will be linear.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fadeout\_time** = `0.0`
`🔗<class_AnimationNodeOneShot_property_fadeout_time>`

classref-property-setget

-   `void (No return value.)` **set\_fadeout\_time**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fadeout\_time**()

The fade-out duration. For example, setting this to `1.0` for a 5 second
length animation will produce a cross-fade that starts at 4 second and
ends at 5 second during the animation.

\*\*Note:\*\* **AnimationNodeOneShot** transitions the current state
after the end of the fading. When
`AnimationNodeOutput<class_AnimationNodeOutput>` is considered as the
most upstream, so the
`fadeout_time<class_AnimationNodeOneShot_property_fadeout_time>` is
scaled depending on the downstream delta. For example, if this value is
set to `1.0` and an
`AnimationNodeTimeScale<class_AnimationNodeTimeScale>` with a value of
`2.0` is chained downstream, the actual processing time will be 0.5
second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MixMode<enum_AnimationNodeOneShot_MixMode>` **mix\_mode** = `0`
`🔗<class_AnimationNodeOneShot_property_mix_mode>`

classref-property-setget

-   `void (No return value.)` **set\_mix\_mode**(value:
    `MixMode<enum_AnimationNodeOneShot_MixMode>`)
-   `MixMode<enum_AnimationNodeOneShot_MixMode>` **get\_mix\_mode**()

The blend type.
