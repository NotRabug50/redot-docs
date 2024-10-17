github\_url  
hide

# VisualShaderNodeIf

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Outputs a 3D vector based on the result of a floating-point comparison
within the visual shader graph.

classref-introduction-group

## Description

This visual shader node has six input ports:

-   Port **1** and **2** provide the two floating-point numbers `a` and
    `b` that will be compared.
-   Port **3** is the tolerance, which allows similar floating-point
    numbers to be considered equal.
-   Ports **4**, **5**, and **6** are the possible outputs, returned if
    `a == b`, `a > b`, or `a < b` respectively.
