github\_url  
hide

# VisualShaderNodeOuterProduct

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Calculates an outer product of two vectors within the visual shader
graph.

classref-introduction-group

## Description

`OuterProduct` treats the first parameter `c` as a column vector (matrix
with one column) and the second parameter `r` as a row vector (matrix
with one row) and does a linear algebraic matrix multiply `c * r`,
yielding a matrix whose number of rows is the number of components in
`c` and whose number of columns is the number of components in `r`.
