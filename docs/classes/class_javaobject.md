github\_url  
hide

# JavaObject

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Represents an object from the Java Native Interface.

classref-introduction-group

## Description

Represents an object from the Java Native Interface. It can be returned
from Java methods called on `JavaClass<class_JavaClass>` or other
**JavaObject**s. See `JavaClassWrapper<class_JavaClassWrapper>` for an
example.

\*\*Note:\*\* This class only works on Android. On any other platform,
this class does nothing.

\*\*Note:\*\* This class is not to be confused with
`JavaScriptObject<class_JavaScriptObject>`.

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

`JavaClass<class_JavaClass>` **get\_java\_class**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_JavaObject_method_get_java_class>`

Returns the `JavaClass<class_JavaClass>` that this object is an instance
of.
