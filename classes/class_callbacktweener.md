github\_url  
hide

# CallbackTweener

**Inherits:** `Tweener<class_Tweener>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Calls the specified method after optional delay.

classref-introduction-group

## Description

**CallbackTweener** is used to call a method in a tweening sequence. See
`Tween.tween_callback<class_Tween_method_tween_callback>` for more usage
information.

The tweener will finish automatically if the callback's target object is
freed.

\*\*Note:\*\* `Tween.tween_callback<class_Tween_method_tween_callback>`
is the only correct way to create **CallbackTweener**. Any
**CallbackTweener** created manually will not function correctly.

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

## Method Descriptions

classref-method

`CallbackTweener<class_CallbackTweener>` **set\_delay**(delay:
`float<class_float>`) `🔗<class_CallbackTweener_method_set_delay>`

Makes the callback call delayed by given time in seconds.

\*\*Example:\*\* Call `Node.queue_free<class_Node_method_queue_free>`
after 2 seconds.

    var tween = get_tree().create_tween()
    tween.tween_callback(queue_free).set_delay(2)
