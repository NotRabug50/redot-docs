github\_url  
hide

# VisualShaderNodeFaceForward

**Inherits:**
`VisualShaderNodeVectorBase<class_VisualShaderNodeVectorBase>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Returns the vector that points in the same direction as a reference
vector within the visual shader graph.

classref-introduction-group

## Description

Translates to `faceforward(N, I, Nref)` in the shader language. The
function has three vector parameters: `N`, the vector to orient, `I`,
the incident vector, and `Nref`, the reference vector. If the dot
product of `I` and `Nref` is smaller than zero the return value is `N`.
Otherwise, `-N` is returned.
