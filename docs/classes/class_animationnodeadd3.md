github\_url  
hide

# AnimationNodeAdd3

**Inherits:** `AnimationNodeSync<class_AnimationNodeSync>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Blends two of three animations additively inside of an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

classref-introduction-group

## Description

A resource to add to an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`. Blends two
animations out of three additively out of three based on the amount
value.

This animation node has three inputs:

-   The base animation to add to
-   A "-add" animation to blend with when the blend amount is negative
-   A "+add" animation to blend with when the blend amount is positive

If the absolute value of the amount is greater than `1.0`, the animation
connected to "in" port is blended with the amplified animation connected
to "-add"/"+add" port.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)
