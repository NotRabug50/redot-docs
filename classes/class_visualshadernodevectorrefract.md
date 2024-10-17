github\_url  
hide

# VisualShaderNodeVectorRefract

**Inherits:**
`VisualShaderNodeVectorBase<class_VisualShaderNodeVectorBase>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Returns the vector that points in the direction of refraction. For use
within the visual shader graph.

classref-introduction-group

## Description

Translated to `refract(I, N, eta)` in the shader language, where `I` is
the incident vector, `N` is the normal vector and `eta` is the ratio of
the indices of the refraction.
