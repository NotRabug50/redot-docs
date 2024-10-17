github\_url  
hide

# AnimationNodeTimeSeek

**Inherits:** `AnimationNode<class_AnimationNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A time-seeking animation node used in
`AnimationTree<class_AnimationTree>`.

classref-introduction-group

## Description

This animation node can be used to cause a seek command to happen to any
sub-children of the animation graph. Use to play an
`Animation<class_Animation>` from the start or a certain playback
position inside the
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

After setting the time and changing the animation playback, the time
seek node automatically goes into sleep mode on the next process frame
by setting its `seek_request` value to `-1.0`.

gdscript

\# Play child animation from the start.
animation\_tree.set("parameters/TimeSeek/seek\_request", 0.0) \#
Alternative syntax (same result as above).
animation\_tree\["parameters/TimeSeek/seek\_request"\] = 0.0

\# Play child animation from 12 second timestamp.
animation\_tree.set("parameters/TimeSeek/seek\_request", 12.0) \#
Alternative syntax (same result as above).
animation\_tree\["parameters/TimeSeek/seek\_request"\] = 12.0

csharp

// Play child animation from the start.
animationTree.Set("parameters/TimeSeek/seek\_request", 0.0);

// Play child animation from 12 second timestamp.
animationTree.Set("parameters/TimeSeek/seek\_request", 12.0);

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
