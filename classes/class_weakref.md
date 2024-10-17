github\_url  
hide

# WeakRef

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Holds an `Object<class_Object>`. If the object is
`RefCounted<class_RefCounted>`, it doesn't update the reference count.

classref-introduction-group

## Description

A weakref can hold a `RefCounted<class_RefCounted>` without contributing
to the reference counter. A weakref can be created from an
`Object<class_Object>` using
`@GlobalScope.weakref<class_@GlobalScope_method_weakref>`. If this
object is not a reference, weakref still works, however, it does not
have any effect on the object. Weakrefs are useful in cases where
multiple classes have variables that refer to each other. Without
weakrefs, using these classes could lead to memory leaks, since both
references keep each other from being released. Making part of the
variables a weakref can prevent this cyclic dependency, and allows the
references to be released.

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

`Variant<class_Variant>` **get\_ref**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WeakRef_method_get_ref>`

Returns the `Object<class_Object>` this weakref is referring to. Returns
`null` if that object no longer exists.
