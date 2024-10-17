github\_url  
hide

# AudioListener3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Overrides the location sounds are heard from.

classref-introduction-group

## Description

Once added to the scene tree and enabled using
`make_current<class_AudioListener3D_method_make_current>`, this node
will override the location sounds are heard from. This can be used to
listen from a location different from the `Camera3D<class_Camera3D>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear\_current**()
`🔗<class_AudioListener3D_method_clear_current>`

Disables the listener to use the current camera's listener instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_listener\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioListener3D_method_get_listener_transform>`

Returns the listener's global orthonormalized
`Transform3D<class_Transform3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_current**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioListener3D_method_is_current>`

Returns `true` if the listener was made current using
`make_current<class_AudioListener3D_method_make_current>`, `false`
otherwise.

\*\*Note:\*\* There may be more than one AudioListener3D marked as
"current" in the scene tree, but only the one that was made current last
will be used.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **make\_current**()
`🔗<class_AudioListener3D_method_make_current>`

Enables the listener. This will override the current camera's listener.
