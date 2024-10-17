github\_url  
hide

# VisualShaderNodeTransformDecompose

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Decomposes a `Transform3D<class_Transform3D>` into four
`Vector3<class_Vector3>`s within the visual shader graph.

classref-introduction-group

## Description

Takes a 4×4 transform matrix and decomposes it into four `vec3` values,
one from each row of the matrix.
