github\_url  
hide

# InstancePlaceholder

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

Placeholder for the root `Node<class_Node>` of a
`PackedScene<class_PackedScene>`.

classref-introduction-group

## Description

Turning on the option **Load As Placeholder** for an instantiated scene
in the editor causes it to be replaced by an **InstancePlaceholder**
when running the game, this will not replace the node in the editor.
This makes it possible to delay actually loading the scene until calling
`create_instance<class_InstancePlaceholder_method_create_instance>`.
This is useful to avoid loading large scenes all at once by loading
parts of it selectively.

The **InstancePlaceholder** does not have a transform. This causes any
child nodes to be positioned relatively to the
`Viewport<class_Viewport>` from point (0,0), rather than their parent as
displayed in the editor. Replacing the placeholder with a scene with a
transform will transform children relatively to their parent again.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Node<class_Node>` **create\_instance**(replace: `bool<class_bool>` =
false, custom\_scene: `PackedScene<class_PackedScene>` = null)
`🔗<class_InstancePlaceholder_method_create_instance>`

Call this method to actually load in the node. The created node will be
placed as a sibling *above* the **InstancePlaceholder** in the scene
tree. The `Node<class_Node>`'s reference is also returned for
convenience.

\*\*Note:\*\*
`create_instance<class_InstancePlaceholder_method_create_instance>` is
not thread-safe. Use
`Object.call_deferred<class_Object_method_call_deferred>` if calling
from a thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_instance\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InstancePlaceholder_method_get_instance_path>`

Gets the path to the `PackedScene<class_PackedScene>` resource file that
is loaded by default when calling
`create_instance<class_InstancePlaceholder_method_create_instance>`. Not
thread-safe. Use
`Object.call_deferred<class_Object_method_call_deferred>` if calling
from a thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_stored\_values**(with\_order:
`bool<class_bool>` = false)
`🔗<class_InstancePlaceholder_method_get_stored_values>`

Returns the list of properties that will be applied to the node when
`create_instance<class_InstancePlaceholder_method_create_instance>` is
called.

If `with_order` is `true`, a key named `.order` (note the leading
period) is added to the dictionary. This `.order` key is an
`Array<class_Array>` of `String<class_String>` property names specifying
the order in which properties will be applied (with index 0 being the
first).
