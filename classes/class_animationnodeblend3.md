github\_url  
hide

# AnimationNodeBlend3

**Inherits:** `AnimationNodeSync<class_AnimationNodeSync>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Blends two of three animations linearly inside of an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

classref-introduction-group

## Description

A resource to add to an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`. Blends two
animations out of three linearly out of three based on the amount value.

This animation node has three inputs:

-   The base animation to blend with
-   A "-blend" animation to blend with when the blend amount is negative
    value
-   A "+blend" animation to blend with when the blend amount is positive
    value

In general, the blend value should be in the `[-1.0, 1.0]` range. Values
outside of this range can blend amplified animations, however,
`AnimationNodeAdd3<class_AnimationNodeAdd3>` works better for this
purpose.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
