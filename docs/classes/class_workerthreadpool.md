github\_url  
hide

# WorkerThreadPool

**Inherits:** `Object<class_Object>`

A singleton that allocates some `Thread<class_Thread>`s on startup, used
to offload tasks to these threads.

classref-introduction-group

## Description

The **WorkerThreadPool** singleton allocates a set of
`Thread<class_Thread>`s (called worker threads) on project startup and
provides methods for offloading tasks to them. This can be used for
simple multithreading without having to create `Thread<class_Thread>`s.

Tasks hold the `Callable<class_Callable>` to be run by the threads.
**WorkerThreadPool** can be used to create regular tasks, which will be
taken by one worker thread, or group tasks, which can be distributed
between multiple worker threads. Group tasks execute the
`Callable<class_Callable>` multiple times, which makes them useful for
iterating over a lot of elements, such as the enemies in an arena.

Here's a sample on how to offload an expensive function to worker
threads:

gdscript

var enemies = \[\] \# An array to be filled with enemies.

func process\_enemy\_ai(enemy\_index):  
var processed\_enemy = enemies\[enemy\_index\] \# Expensive logic...

func \_process(delta):  
var task\_id = WorkerThreadPool.add\_group\_task(process\_enemy\_ai,
enemies.size()) \# Other code...
WorkerThreadPool.wait\_for\_group\_task\_completion(task\_id) \# Other
code that depends on the enemy AI already being processed.

csharp

private List&lt;Node&gt; \_enemies = new List&lt;Node&gt;(); // A list
to be filled with enemies.

private void ProcessEnemyAI(int enemyIndex) { Node processedEnemy =
\_enemies\[enemyIndex\]; // Expensive logic here. }

public override void \_Process(double delta) { long taskId =
WorkerThreadPool.AddGroupTask(Callable.From&lt;int&gt;(ProcessEnemyAI),
\_enemies.Count); // Other code...
WorkerThreadPool.WaitForGroupTaskCompletion(taskId); // Other code that
depends on the enemy AI already being processed. }

The above code relies on the number of elements in the `enemies` array
remaining constant during the multithreaded part.

\*\*Note:\*\* Using this singleton could affect performance negatively
if the task being distributed between threads is not computationally
expensive.

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

`int<class_int>` **add\_group\_task**(action:
`Callable<class_Callable>`, elements: `int<class_int>`, tasks\_needed:
`int<class_int>` = -1, high\_priority: `bool<class_bool>` = false,
description: `String<class_String>` = "")
`🔗<class_WorkerThreadPool_method_add_group_task>`

Adds `action` as a group task to be executed by the worker threads. The
`Callable<class_Callable>` will be called a number of times based on
`elements`, with the first thread calling it with the value `0` as a
parameter, and each consecutive execution incrementing this value by 1
until it reaches `element - 1`.

The number of threads the task is distributed to is defined by
`tasks_needed`, where the default value `-1` means it is distributed to
all worker threads. `high_priority` determines if the task has a high
priority or a low priority (default). You can optionally provide a
`description` to help with debugging.

Returns a group task ID that can be used by other methods.

\*\*Warning:\*\* Every task must be waited for completion using
`wait_for_task_completion<class_WorkerThreadPool_method_wait_for_task_completion>`
or
`wait_for_group_task_completion<class_WorkerThreadPool_method_wait_for_group_task_completion>`
at some point so that any allocated resources inside the task can be
cleaned up.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **add\_task**(action: `Callable<class_Callable>`,
high\_priority: `bool<class_bool>` = false, description:
`String<class_String>` = "")
`🔗<class_WorkerThreadPool_method_add_task>`

Adds `action` as a task to be executed by a worker thread.
`high_priority` determines if the task has a high priority or a low
priority (default). You can optionally provide a `description` to help
with debugging.

Returns a task ID that can be used by other methods.

\*\*Warning:\*\* Every task must be waited for completion using
`wait_for_task_completion<class_WorkerThreadPool_method_wait_for_task_completion>`
or
`wait_for_group_task_completion<class_WorkerThreadPool_method_wait_for_group_task_completion>`
at some point so that any allocated resources inside the task can be
cleaned up.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_group\_processed\_element\_count**(group\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WorkerThreadPool_method_get_group_processed_element_count>`

Returns how many times the `Callable<class_Callable>` of the group task
with the given ID has already been executed by the worker threads.

\*\*Note:\*\* If a thread has started executing the
`Callable<class_Callable>` but is yet to finish, it won't be counted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_group\_task\_completed**(group\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WorkerThreadPool_method_is_group_task_completed>`

Returns `true` if the group task with the given ID is completed.

\*\*Note:\*\* You should only call this method between adding the group
task and awaiting its completion.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_task\_completed**(task\_id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WorkerThreadPool_method_is_task_completed>`

Returns `true` if the task with the given ID is completed.

\*\*Note:\*\* You should only call this method between adding the task
and awaiting its completion.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**wait\_for\_group\_task\_completion**(group\_id: `int<class_int>`)
`🔗<class_WorkerThreadPool_method_wait_for_group_task_completion>`

Pauses the thread that calls this method until the group task with the
given ID is completed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**wait\_for\_task\_completion**(task\_id: `int<class_int>`)
`🔗<class_WorkerThreadPool_method_wait_for_task_completion>`

Pauses the thread that calls this method until the task with the given
ID is completed.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` if the task
could be successfully awaited.

Returns
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
if a task with the passed ID does not exist (maybe because it was
already awaited and disposed of).

Returns `@GlobalScope.ERR_BUSY<class_@GlobalScope_constant_ERR_BUSY>` if
the call is made from another running task and, due to task scheduling,
there's potential for deadlocking (e.g., the task to await may be at a
lower level in the call stack and therefore can't progress). This is an
advanced situation that should only matter when some tasks depend on
others (in the current implementation, the tricky case is a task trying
to wait on an older one).
