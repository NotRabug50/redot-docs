github\_url  
hide

# AnimationNodeAdd2

**Inherits:** `AnimationNodeSync<class_AnimationNodeSync>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Blends two animations additively inside of an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

classref-introduction-group

## Description

A resource to add to an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`. Blends two
animations additively based on the amount value.

If the amount is greater than `1.0`, the animation connected to "in"
port is blended with the amplified animation connected to "add" port.

If the amount is less than `0.0`, the animation connected to "in" port
is blended with the inverted animation connected to "add" port.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
