github\_url  
hide

# Semaphore

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

A synchronization mechanism used to control access to a shared resource
by `Thread<class_Thread>`s.

classref-introduction-group

## Description

A synchronization semaphore that can be used to synchronize multiple
`Thread<class_Thread>`s. Initialized to zero on creation. For a binary
version, see `Mutex<class_Mutex>`.

\*\*Warning:\*\* Semaphores must be used carefully to avoid deadlocks.

\*\*Warning:\*\* To guarantee that the operating system is able to
perform proper cleanup (no crashes, no deadlocks), these conditions must
be met:

-   When a **Semaphore**'s reference count reaches zero and it is
    therefore destroyed, no threads must be waiting on it.
-   When a `Thread<class_Thread>`'s reference count reaches zero and it
    is therefore destroyed, it must not be waiting on any semaphore.

classref-introduction-group

## Tutorials

-   `Using multiple threads <../tutorials/performance/using_multiple_threads>`
-   `Thread-safe APIs <../tutorials/performance/thread_safe_apis>`

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

`void (No return value.)` **post**(count: `int<class_int>` = 1)
`🔗<class_Semaphore_method_post>`

Lowers the **Semaphore**, allowing one thread in, or more if `count` is
specified.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **try\_wait**() `🔗<class_Semaphore_method_try_wait>`

Like `wait<class_Semaphore_method_wait>`, but won't block, so if the
value is zero, fails immediately and returns `false`. If non-zero, it
returns `true` to report success.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **wait**() `🔗<class_Semaphore_method_wait>`

Waits for the **Semaphore**, if its value is zero, blocks until
non-zero.
