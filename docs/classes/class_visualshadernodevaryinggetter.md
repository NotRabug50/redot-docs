github\_url  
hide

# VisualShaderNodeVaryingGetter

**Inherits:** `VisualShaderNodeVarying<class_VisualShaderNodeVarying>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A visual shader node that gets a value of a varying.

classref-introduction-group

## Description

Outputs a value of a varying defined in the shader. You need to first
create a varying that can be used in the given function, e.g. varying
getter in Fragment shader requires a varying with mode set to
`VisualShader.VARYING_MODE_VERTEX_TO_FRAG_LIGHT<class_VisualShader_constant_VARYING_MODE_VERTEX_TO_FRAG_LIGHT>`.
