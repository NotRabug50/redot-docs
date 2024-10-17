github\_url  
hide

# AnimationNodeBlend2

**Inherits:** `AnimationNodeSync<class_AnimationNodeSync>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Blends two animations linearly inside of an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

classref-introduction-group

## Description

A resource to add to an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`. Blends two
animations linearly based on the amount value.

In general, the blend value should be in the `[0.0, 1.0]` range. Values
outside of this range can blend amplified or inverted animations,
however, `AnimationNodeAdd2<class_AnimationNodeAdd2>` works better for
this purpose.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)
