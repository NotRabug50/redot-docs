github\_url  
hide

# JavaClassWrapper

**Inherits:** `Object<class_Object>`

Provides access to the Java Native Interface.

classref-introduction-group

## Description

The JavaClassWrapper singleton provides a way for the Godot application
to send and receive data through the [Java Native
Interface](https://developer.android.com/training/articles/perf-jni)
(JNI).

\*\*Note:\*\* This singleton is only available in Android builds.

    var LocalDateTime = JavaClassWrapper.wrap("java.time.LocalDateTime")
    var DateTimeFormatter = JavaClassWrapper.wrap("java.time.format.DateTimeFormatter")

    var datetime = LocalDateTime.now()
    var formatter = DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss")

    print(datetime.format(formatter))

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

`JavaClass<class_JavaClass>` **wrap**(name: `String<class_String>`)
`🔗<class_JavaClassWrapper_method_wrap>`

Wraps a class defined in Java, and returns it as a
`JavaClass<class_JavaClass>` `Object<class_Object>` type that Godot can
interact with.

\*\*Note:\*\* This method only works on Android. On every other
platform, this method does nothing and returns an empty
`JavaClass<class_JavaClass>`.
