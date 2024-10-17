github\_url  
hide

# Tween

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Lightweight object used for general-purpose animation via script, using
`Tweener<class_Tweener>`s.

classref-introduction-group

## Description

Tweens are mostly useful for animations requiring a numerical property
to be interpolated over a range of values. The name *tween* comes from
*in-betweening*, an animation technique where you specify *keyframes*
and the computer interpolates the frames that appear between them.
Animating something with a **Tween** is called tweening.

\*\*Tween\*\* is more suited than
`AnimationPlayer<class_AnimationPlayer>` for animations where you don't
know the final values in advance. For example, interpolating a
dynamically-chosen camera zoom value is best done with a **Tween**; it
would be difficult to do the same thing with an
`AnimationPlayer<class_AnimationPlayer>` node. Tweens are also more
light-weight than `AnimationPlayer<class_AnimationPlayer>`, so they are
very much suited for simple animations or general tasks that don't
require visual tweaking provided by the editor. They can be used in a
"fire-and-forget" manner for some logic that normally would be done by
code. You can e.g. make something shoot periodically by using a looped
`CallbackTweener<class_CallbackTweener>` with a delay.

A **Tween** can be created by using either
`SceneTree.create_tween<class_SceneTree_method_create_tween>` or
`Node.create_tween<class_Node_method_create_tween>`. **Tween**s created
manually (i.e. by using `Tween.new()`) are invalid and can't be used for
tweening values.

A tween animation is created by adding `Tweener<class_Tweener>`s to the
**Tween** object, using
`tween_property<class_Tween_method_tween_property>`,
`tween_interval<class_Tween_method_tween_interval>`,
`tween_callback<class_Tween_method_tween_callback>` or
`tween_method<class_Tween_method_tween_method>`:

gdscript

var tween = get\_tree().create\_tween() tween.tween\_property($Sprite,
"modulate", Color.RED, 1) tween.tween\_property($Sprite, "scale",
Vector2(), 1) tween.tween\_callback($Sprite.queue\_free)

csharp

Tween tween = GetTree().CreateTween();
tween.TweenProperty(GetNode("Sprite"), "modulate", Colors.Red, 1.0f);
tween.TweenProperty(GetNode("Sprite"), "scale", Vector2.Zero, 1.0f);
tween.TweenCallback(Callable.From(GetNode("Sprite").QueueFree));

This sequence will make the `$Sprite` node turn red, then shrink, before
finally calling `Node.queue_free<class_Node_method_queue_free>` to free
the sprite. `Tweener<class_Tweener>`s are executed one after another by
default. This behavior can be changed using
`parallel<class_Tween_method_parallel>` and
`set_parallel<class_Tween_method_set_parallel>`.

When a `Tweener<class_Tweener>` is created with one of the `tween_*`
methods, a chained method call can be used to tweak the properties of
this `Tweener<class_Tweener>`. For example, if you want to set a
different transition type in the above example, you can use
`set_trans<class_Tween_method_set_trans>`:

gdscript

var tween = get\_tree().create\_tween() tween.tween\_property($Sprite,
"modulate", Color.RED, 1).set\_trans(Tween.TRANS\_SINE)
tween.tween\_property($Sprite, "scale", Vector2(),
1).set\_trans(Tween.TRANS\_BOUNCE)
tween.tween\_callback($Sprite.queue\_free)

csharp

Tween tween = GetTree().CreateTween();
tween.TweenProperty(GetNode("Sprite"), "modulate", Colors.Red,
1.0f).SetTrans(Tween.TransitionType.Sine);
tween.TweenProperty(GetNode("Sprite"), "scale", Vector2.Zero,
1.0f).SetTrans(Tween.TransitionType.Bounce);
tween.TweenCallback(Callable.From(GetNode("Sprite").QueueFree));

Most of the **Tween** methods can be chained this way too. In the
following example the **Tween** is bound to the running script's node
and a default transition is set for its `Tweener<class_Tweener>`s:

gdscript

var tween =
get\_tree().create\_tween().bind\_node(self).set\_trans(Tween.TRANS\_ELASTIC)
tween.tween\_property($Sprite, "modulate", Color.RED, 1)
tween.tween\_property($Sprite, "scale", Vector2(), 1)
tween.tween\_callback($Sprite.queue\_free)

csharp

var tween =
GetTree().CreateTween().BindNode(this).SetTrans(Tween.TransitionType.Elastic);
tween.TweenProperty(GetNode("Sprite"), "modulate", Colors.Red, 1.0f);
tween.TweenProperty(GetNode("Sprite"), "scale", Vector2.Zero, 1.0f);
tween.TweenCallback(Callable.From(GetNode("Sprite").QueueFree));

Another interesting use for **Tween**s is animating arbitrary sets of
objects:

gdscript

var tween = create\_tween() for sprite in get\_children():
tween.tween\_property(sprite, "position", Vector2(0, 0), 1)

csharp

Tween tween = CreateTween(); foreach (Node sprite in GetChildren())
tween.TweenProperty(sprite, "position", Vector2.Zero, 1.0f);

In the example above, all children of a node are moved one after another
to position (0, 0).

You should avoid using more than one **Tween** per object's property. If
two or more tweens animate one property at the same time, the last one
created will take priority and assign the final value. If you want to
interrupt and restart an animation, consider assigning the **Tween** to
a variable:

gdscript

var tween func animate(): if tween: tween.kill() \# Abort the previous
animation. tween = create\_tween()

csharp

private Tween \_tween;

public void Animate() { if (\_tween != null) \_tween.Kill(); // Abort
the previous animation \_tween = CreateTween(); }

Some `Tweener<class_Tweener>`s use transitions and eases. The first
accepts a `TransitionType<enum_Tween_TransitionType>` constant, and
refers to the way the timing of the animation is handled (see
[easings.net](https://easings.net/) for some examples). The second
accepts an `EaseType<enum_Tween_EaseType>` constant, and controls where
the `trans_type` is applied to the interpolation (in the beginning, the
end, or both). If you don't know which transition and easing to pick,
you can try different `TransitionType<enum_Tween_TransitionType>`
constants with `EASE_IN_OUT<class_Tween_constant_EASE_IN_OUT>`, and use
the one that looks best.

[Tween easing and transition types
cheatsheet](https://raw.githubusercontent.com/godotengine/godot-docs/master/img/tween_cheatsheet.webp)

\*\*Note:\*\* Tweens are not designed to be re-used and trying to do so
results in an undefined behavior. Create a new Tween for each animation
and every time you replay an animation from start. Keep in mind that
Tweens start immediately, so only create a Tween when you want to start
animating.

\*\*Note:\*\* The tween is processed after all of the nodes in the
current frame, i.e. node's
`Node._process<class_Node_private_method__process>` method would be
called before the tween (or
`Node._physics_process<class_Node_private_method__physics_process>`
depending on the value passed to
`set_process_mode<class_Tween_method_set_process_mode>`).

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**finished**() `🔗<class_Tween_signal_finished>`

Emitted when the **Tween** has finished all tweening. Never emitted when
the **Tween** is set to infinite looping (see
`set_loops<class_Tween_method_set_loops>`).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**loop\_finished**(loop\_count: `int<class_int>`)
`🔗<class_Tween_signal_loop_finished>`

Emitted when a full loop is complete (see
`set_loops<class_Tween_method_set_loops>`), providing the loop index.
This signal is not emitted after the final loop, use
`finished<class_Tween_signal_finished>` instead for this case.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**step\_finished**(idx: `int<class_int>`)
`🔗<class_Tween_signal_step_finished>`

Emitted when one step of the **Tween** is complete, providing the step
index. One step is either a single `Tweener<class_Tweener>` or a group
of `Tweener<class_Tweener>`s running in parallel.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TweenProcessMode**: `🔗<enum_Tween_TweenProcessMode>`

classref-enumeration-constant

`TweenProcessMode<enum_Tween_TweenProcessMode>`
**TWEEN\_PROCESS\_PHYSICS** = `0`

The **Tween** updates after each physics frame (see
`Node._physics_process<class_Node_private_method__physics_process>`).

classref-enumeration-constant

`TweenProcessMode<enum_Tween_TweenProcessMode>` **TWEEN\_PROCESS\_IDLE**
= `1`

The **Tween** updates after each process frame (see
`Node._process<class_Node_private_method__process>`).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TweenPauseMode**: `🔗<enum_Tween_TweenPauseMode>`

classref-enumeration-constant

`TweenPauseMode<enum_Tween_TweenPauseMode>` **TWEEN\_PAUSE\_BOUND** =
`0`

If the **Tween** has a bound node, it will process when that node can
process (see `Node.process_mode<class_Node_property_process_mode>`).
Otherwise it's the same as
`TWEEN_PAUSE_STOP<class_Tween_constant_TWEEN_PAUSE_STOP>`.

classref-enumeration-constant

`TweenPauseMode<enum_Tween_TweenPauseMode>` **TWEEN\_PAUSE\_STOP** = `1`

If `SceneTree<class_SceneTree>` is paused, the **Tween** will also
pause.

classref-enumeration-constant

`TweenPauseMode<enum_Tween_TweenPauseMode>` **TWEEN\_PAUSE\_PROCESS** =
`2`

The **Tween** will process regardless of whether
`SceneTree<class_SceneTree>` is paused.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TransitionType**: `🔗<enum_Tween_TransitionType>`

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_LINEAR** = `0`

The animation is interpolated linearly.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_SINE** = `1`

The animation is interpolated using a sine function.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_QUINT** = `2`

The animation is interpolated with a quintic (to the power of 5)
function.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_QUART** = `3`

The animation is interpolated with a quartic (to the power of 4)
function.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_QUAD** = `4`

The animation is interpolated with a quadratic (to the power of 2)
function.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_EXPO** = `5`

The animation is interpolated with an exponential (to the power of x)
function.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_ELASTIC** = `6`

The animation is interpolated with elasticity, wiggling around the
edges.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_CUBIC** = `7`

The animation is interpolated with a cubic (to the power of 3) function.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_CIRC** = `8`

The animation is interpolated with a function using square roots.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_BOUNCE** = `9`

The animation is interpolated by bouncing at the end.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_BACK** = `10`

The animation is interpolated backing out at ends.

classref-enumeration-constant

`TransitionType<enum_Tween_TransitionType>` **TRANS\_SPRING** = `11`

The animation is interpolated like a spring towards the end.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EaseType**: `🔗<enum_Tween_EaseType>`

classref-enumeration-constant

`EaseType<enum_Tween_EaseType>` **EASE\_IN** = `0`

The interpolation starts slowly and speeds up towards the end.

classref-enumeration-constant

`EaseType<enum_Tween_EaseType>` **EASE\_OUT** = `1`

The interpolation starts quickly and slows down towards the end.

classref-enumeration-constant

`EaseType<enum_Tween_EaseType>` **EASE\_IN\_OUT** = `2`

A combination of `EASE_IN<class_Tween_constant_EASE_IN>` and
`EASE_OUT<class_Tween_constant_EASE_OUT>`. The interpolation is slowest
at both ends.

classref-enumeration-constant

`EaseType<enum_Tween_EaseType>` **EASE\_OUT\_IN** = `3`

A combination of `EASE_IN<class_Tween_constant_EASE_IN>` and
`EASE_OUT<class_Tween_constant_EASE_OUT>`. The interpolation is fastest
at both ends.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Tween<class_Tween>` **bind\_node**(node: `Node<class_Node>`)
`🔗<class_Tween_method_bind_node>`

Binds this **Tween** with the given `node`. **Tween**s are processed
directly by the `SceneTree<class_SceneTree>`, so they run independently
of the animated nodes. When you bind a `Node<class_Node>` with the
**Tween**, the **Tween** will halt the animation when the object is not
inside tree and the **Tween** will be automatically killed when the
bound object is freed. Also
`TWEEN_PAUSE_BOUND<class_Tween_constant_TWEEN_PAUSE_BOUND>` will make
the pausing behavior dependent on the bound node.

For a shorter way to create and bind a **Tween**, you can use
`Node.create_tween<class_Node_method_create_tween>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **chain**() `🔗<class_Tween_method_chain>`

Used to chain two `Tweener<class_Tweener>`s after
`set_parallel<class_Tween_method_set_parallel>` is called with `true`.

gdscript

var tween = create\_tween().set\_parallel(true)
tween.tween\_property(...) tween.tween\_property(...) \# Will run
parallelly with above. tween.chain().tween\_property(...) \# Will run
after two above are finished.

csharp

Tween tween = CreateTween().SetParallel(true); tween.TweenProperty(...);
tween.TweenProperty(...); // Will run parallelly with above.
tween.Chain().TweenProperty(...); // Will run after two above are
finished.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **custom\_step**(delta: `float<class_float>`)
`🔗<class_Tween_method_custom_step>`

Processes the **Tween** by the given `delta` value, in seconds. This is
mostly useful for manual control when the **Tween** is paused. It can
also be used to end the **Tween** animation immediately, by setting
`delta` longer than the whole duration of the **Tween** animation.

Returns `true` if the **Tween** still has `Tweener<class_Tweener>`s that
haven't finished.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_loops\_left**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tween_method_get_loops_left>`

Returns the number of remaining loops for this **Tween** (see
`set_loops<class_Tween_method_set_loops>`). A return value of `-1`
indicates an infinitely looping **Tween**, and a return value of `0`
indicates that the **Tween** has already finished.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_total\_elapsed\_time**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tween_method_get_total_elapsed_time>`

Returns the total time in seconds the **Tween** has been animating (i.e.
the time since it started, not counting pauses etc.). The time is
affected by `set_speed_scale<class_Tween_method_set_speed_scale>`, and
`stop<class_Tween_method_stop>` will reset it to `0`.

\*\*Note:\*\* As it results from accumulating frame deltas, the time
returned after the **Tween** has finished animating will be slightly
greater than the actual **Tween** duration.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **interpolate\_value**(initial\_value:
`Variant<class_Variant>`, delta\_value: `Variant<class_Variant>`,
elapsed\_time: `float<class_float>`, duration: `float<class_float>`,
trans\_type: `TransitionType<enum_Tween_TransitionType>`, ease\_type:
`EaseType<enum_Tween_EaseType>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_Tween_method_interpolate_value>`

This method can be used for manual interpolation of a value, when you
don't want **Tween** to do animating for you. It's similar to
`@GlobalScope.lerp<class_@GlobalScope_method_lerp>`, but with support
for custom transition and easing.

`initial_value` is the starting value of the interpolation.

`delta_value` is the change of the value in the interpolation, i.e. it's
equal to `final_value - initial_value`.

`elapsed_time` is the time in seconds that passed after the
interpolation started and it's used to control the position of the
interpolation. E.g. when it's equal to half of the `duration`, the
interpolated value will be halfway between initial and final values.
This value can also be greater than `duration` or lower than 0, which
will extrapolate the value.

`duration` is the total time of the interpolation.

\*\*Note:\*\* If `duration` is equal to `0`, the method will always
return the final value, regardless of `elapsed_time` provided.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_running**() `🔗<class_Tween_method_is_running>`

Returns whether the **Tween** is currently running, i.e. it wasn't
paused and it's not finished.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid**() `🔗<class_Tween_method_is_valid>`

Returns whether the **Tween** is valid. A valid **Tween** is a **Tween**
contained by the scene tree (i.e. the array from
`SceneTree.get_processed_tweens<class_SceneTree_method_get_processed_tweens>`
will contain this **Tween**). A **Tween** might become invalid when it
has finished tweening, is killed, or when created with `Tween.new()`.
Invalid **Tween**s can't have `Tweener<class_Tweener>`s appended.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **kill**() `🔗<class_Tween_method_kill>`

Aborts all tweening operations and invalidates the **Tween**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **parallel**() `🔗<class_Tween_method_parallel>`

Makes the next `Tweener<class_Tweener>` run parallelly to the previous
one.

gdscript

var tween = create\_tween() tween.tween\_property(...)
tween.parallel().tween\_property(...)
tween.parallel().tween\_property(...)

csharp

Tween tween = CreateTween(); tween.TweenProperty(...);
tween.Parallel().TweenProperty(...);
tween.Parallel().TweenProperty(...);

All `Tweener<class_Tweener>`s in the example will run at the same time.

You can make the **Tween** parallel by default by using
`set_parallel<class_Tween_method_set_parallel>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pause**() `🔗<class_Tween_method_pause>`

Pauses the tweening. The animation can be resumed by using
`play<class_Tween_method_play>`.

\*\*Note:\*\* If a Tween is paused and not bound to any node, it will
exist indefinitely until manually started or invalidated. If you lose a
reference to such Tween, you can retrieve it using
`SceneTree.get_processed_tweens<class_SceneTree_method_get_processed_tweens>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play**() `🔗<class_Tween_method_play>`

Resumes a paused or stopped **Tween**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **set\_ease**(ease:
`EaseType<enum_Tween_EaseType>`) `🔗<class_Tween_method_set_ease>`

Sets the default ease type for `PropertyTweener<class_PropertyTweener>`s
and `MethodTweener<class_MethodTweener>`s animated by this **Tween**.

If not specified, the default value is
`EASE_IN_OUT<class_Tween_constant_EASE_IN_OUT>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **set\_loops**(loops: `int<class_int>` = 0)
`🔗<class_Tween_method_set_loops>`

Sets the number of times the tweening sequence will be repeated, i.e.
`set_loops(2)` will run the animation twice.

Calling this method without arguments will make the **Tween** run
infinitely, until either it is killed with
`kill<class_Tween_method_kill>`, the **Tween**'s bound node is freed, or
all the animated objects have been freed (which makes further animation
impossible).

\*\*Warning:\*\* Make sure to always add some duration/delay when using
infinite loops. To prevent the game freezing, 0-duration looped
animations (e.g. a single `CallbackTweener<class_CallbackTweener>` with
no delay) are stopped after a small number of loops, which may produce
unexpected results. If a **Tween**'s lifetime depends on some node,
always use `bind_node<class_Tween_method_bind_node>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **set\_parallel**(parallel: `bool<class_bool>` =
true) `🔗<class_Tween_method_set_parallel>`

If `parallel` is `true`, the `Tweener<class_Tweener>`s appended after
this method will by default run simultaneously, as opposed to
sequentially.

\*\*Note:\*\* Just like with `parallel<class_Tween_method_parallel>`,
the tweener added right before this method will also be part of the
parallel step.

    tween.tween_property(self, "position", Vector2(300, 0), 0.5)
    tween.set_parallel()
    tween.tween_property(self, "modulate", Color.GREEN, 0.5) # Runs together with the position tweener.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **set\_pause\_mode**(mode:
`TweenPauseMode<enum_Tween_TweenPauseMode>`)
`🔗<class_Tween_method_set_pause_mode>`

Determines the behavior of the **Tween** when the
`SceneTree<class_SceneTree>` is paused. Check
`TweenPauseMode<enum_Tween_TweenPauseMode>` for options.

Default value is
`TWEEN_PAUSE_BOUND<class_Tween_constant_TWEEN_PAUSE_BOUND>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **set\_process\_mode**(mode:
`TweenProcessMode<enum_Tween_TweenProcessMode>`)
`🔗<class_Tween_method_set_process_mode>`

Determines whether the **Tween** should run after process frames (see
`Node._process<class_Node_private_method__process>`) or physics frames
(see
`Node._physics_process<class_Node_private_method__physics_process>`).

Default value is
`TWEEN_PROCESS_IDLE<class_Tween_constant_TWEEN_PROCESS_IDLE>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **set\_speed\_scale**(speed: `float<class_float>`)
`🔗<class_Tween_method_set_speed_scale>`

Scales the speed of tweening. This affects all `Tweener<class_Tweener>`s
and their delays.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **set\_trans**(trans:
`TransitionType<enum_Tween_TransitionType>`)
`🔗<class_Tween_method_set_trans>`

Sets the default transition type for
`PropertyTweener<class_PropertyTweener>`s and
`MethodTweener<class_MethodTweener>`s animated by this **Tween**.

If not specified, the default value is
`TRANS_LINEAR<class_Tween_constant_TRANS_LINEAR>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**() `🔗<class_Tween_method_stop>`

Stops the tweening and resets the **Tween** to its initial state. This
will not remove any appended `Tweener<class_Tweener>`s.

\*\*Note:\*\* If a Tween is stopped and not bound to any node, it will
exist indefinitely until manually started or invalidated. If you lose a
reference to such Tween, you can retrieve it using
`SceneTree.get_processed_tweens<class_SceneTree_method_get_processed_tweens>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CallbackTweener<class_CallbackTweener>` **tween\_callback**(callback:
`Callable<class_Callable>`) `🔗<class_Tween_method_tween_callback>`

Creates and appends a `CallbackTweener<class_CallbackTweener>`. This
method can be used to call an arbitrary method in any object. Use
`Callable.bind<class_Callable_method_bind>` to bind additional arguments
for the call.

\*\*Example:\*\* Object that keeps shooting every 1 second:

gdscript

var tween = get\_tree().create\_tween().set\_loops()
tween.tween\_callback(shoot).set\_delay(1)

csharp

Tween tween = GetTree().CreateTween().SetLoops();
tween.TweenCallback(Callable.From(Shoot)).SetDelay(1.0f);

\*\*Example:\*\* Turning a sprite red and then blue, with 2 second
delay:

gdscript

var tween = get\_tree().create\_tween()
tween.tween\_callback($Sprite.set\_modulate.bind(Color.RED)).set\_delay(2)
tween.tween\_callback($Sprite.set\_modulate.bind(Color.BLUE)).set\_delay(2)

csharp

Tween tween = GetTree().CreateTween(); Sprite2D sprite =
GetNode&lt;Sprite2D&gt;("Sprite"); tween.TweenCallback(Callable.From(()
=&gt; sprite.Modulate = Colors.Red)).SetDelay(2.0f);
tween.TweenCallback(Callable.From(() =&gt; sprite.Modulate =
Colors.Blue)).SetDelay(2.0f);

classref-item-separator

------------------------------------------------------------------------

classref-method

`IntervalTweener<class_IntervalTweener>` **tween\_interval**(time:
`float<class_float>`) `🔗<class_Tween_method_tween_interval>`

Creates and appends an `IntervalTweener<class_IntervalTweener>`. This
method can be used to create delays in the tween animation, as an
alternative to using the delay in other `Tweener<class_Tweener>`s, or
when there's no animation (in which case the **Tween** acts as a timer).
`time` is the length of the interval, in seconds.

\*\*Example:\*\* Creating an interval in code execution:

gdscript

\# ... some code await create\_tween().tween\_interval(2).finished \#
... more code

csharp

// ... some code await ToSignal(CreateTween().TweenInterval(2.0f),
Tween.SignalName.Finished); // ... more code

\*\*Example:\*\* Creating an object that moves back and forth and jumps
every few seconds:

gdscript

var tween = create\_tween().set\_loops() tween.tween\_property($Sprite,
"position:x", 200.0, 1).as\_relative() tween.tween\_callback(jump)
tween.tween\_interval(2) tween.tween\_property($Sprite, "position:x",
-200.0, 1).as\_relative() tween.tween\_callback(jump)
tween.tween\_interval(2)

csharp

Tween tween = CreateTween().SetLoops();
tween.TweenProperty(GetNode("Sprite"), "position:x", 200.0f,
1.0f).AsRelative(); tween.TweenCallback(Callable.From(Jump));
tween.TweenInterval(2.0f); tween.TweenProperty(GetNode("Sprite"),
"position:x", -200.0f, 1.0f).AsRelative();
tween.TweenCallback(Callable.From(Jump)); tween.TweenInterval(2.0f);

classref-item-separator

------------------------------------------------------------------------

classref-method

`MethodTweener<class_MethodTweener>` **tween\_method**(method:
`Callable<class_Callable>`, from: `Variant<class_Variant>`, to:
`Variant<class_Variant>`, duration: `float<class_float>`)
`🔗<class_Tween_method_tween_method>`

Creates and appends a `MethodTweener<class_MethodTweener>`. This method
is similar to a combination of
`tween_callback<class_Tween_method_tween_callback>` and
`tween_property<class_Tween_method_tween_property>`. It calls a method
over time with a tweened value provided as an argument. The value is
tweened between `from` and `to` over the time specified by `duration`,
in seconds. Use `Callable.bind<class_Callable_method_bind>` to bind
additional arguments for the call. You can use
`MethodTweener.set_ease<class_MethodTweener_method_set_ease>` and
`MethodTweener.set_trans<class_MethodTweener_method_set_trans>` to tweak
the easing and transition of the value or
`MethodTweener.set_delay<class_MethodTweener_method_set_delay>` to delay
the tweening.

\*\*Example:\*\* Making a 3D object look from one point to another
point:

gdscript

var tween = create\_tween()
tween.tween\_method(look\_at.bind(Vector3.UP), Vector3(-1, 0, -1),
Vector3(1, 0, -1), 1) \# The look\_at() method takes up vector as second
argument.

csharp

Tween tween = CreateTween(); tween.TweenMethod(Callable.From((Vector3
target) =&gt; LookAt(target, Vector3.Up)), new Vector3(-1.0f, 0.0f,
-1.0f), new Vector3(1.0f, 0.0f, -1.0f), 1.0f); // Use lambdas to bind
additional arguments for the call.

\*\*Example:\*\* Setting the text of a `Label<class_Label>`, using an
intermediate method and after a delay:

gdscript

func \_ready():  
var tween = create\_tween() tween.tween\_method(set\_label\_text, 0, 10,
1).set\_delay(1)

func set\_label\_text(value: int):  
$Label.text = "Counting " + str(value)

csharp

public override void \_Ready() { base.\_Ready();

> Tween tween = CreateTween();
> tween.TweenMethod(Callable.From&lt;int&gt;(SetLabelText), 0.0f, 10.0f,
> 1.0f).SetDelay(1.0f);

}

private void SetLabelText(int value) {
GetNode&lt;Label&gt;("Label").Text = $"Counting {value}"; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`PropertyTweener<class_PropertyTweener>` **tween\_property**(object:
`Object<class_Object>`, property: `NodePath<class_NodePath>`,
final\_val: `Variant<class_Variant>`, duration: `float<class_float>`)
`🔗<class_Tween_method_tween_property>`

Creates and appends a `PropertyTweener<class_PropertyTweener>`. This
method tweens a `property` of an `object` between an initial value and
`final_val` in a span of time equal to `duration`, in seconds. The
initial value by default is the property's value at the time the
tweening of the `PropertyTweener<class_PropertyTweener>` starts.

gdscript

var tween = create\_tween() tween.tween\_property($Sprite, "position",
Vector2(100, 200), 1) tween.tween\_property($Sprite, "position",
Vector2(200, 300), 1)

csharp

Tween tween = CreateTween(); tween.TweenProperty(GetNode("Sprite"),
"position", new Vector2(100.0f, 200.0f), 1.0f);
tween.TweenProperty(GetNode("Sprite"), "position", new Vector2(200.0f,
300.0f), 1.0f);

will move the sprite to position (100, 200) and then to (200, 300). If
you use `PropertyTweener.from<class_PropertyTweener_method_from>` or
`PropertyTweener.from_current<class_PropertyTweener_method_from_current>`,
the starting position will be overwritten by the given value instead.
See other methods in `PropertyTweener<class_PropertyTweener>` to see how
the tweening can be tweaked further.

\*\*Note:\*\* You can find the correct property name by hovering over
the property in the Inspector. You can also provide the components of a
property directly by using `"property:component"` (eg. `position:x`),
where it would only apply to that particular component.

\*\*Example:\*\* Moving an object twice from the same position, with
different transition types:

gdscript

var tween = create\_tween() tween.tween\_property($Sprite, "position",
Vector2.RIGHT \* 300, 1).as\_relative().set\_trans(Tween.TRANS\_SINE)
tween.tween\_property($Sprite, "position", Vector2.RIGHT \* 300,
1).as\_relative().from\_current().set\_trans(Tween.TRANS\_EXPO)

csharp

Tween tween = CreateTween(); tween.TweenProperty(GetNode("Sprite"),
"position", Vector2.Right \* 300.0f,
1.0f).AsRelative().SetTrans(Tween.TransitionType.Sine);
tween.TweenProperty(GetNode("Sprite"), "position", Vector2.Right \*
300.0f,
1.0f).AsRelative().FromCurrent().SetTrans(Tween.TransitionType.Expo);
