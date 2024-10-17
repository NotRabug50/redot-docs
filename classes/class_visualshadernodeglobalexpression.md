github\_url  
hide

# VisualShaderNodeGlobalExpression

**Inherits:**
`VisualShaderNodeExpression<class_VisualShaderNodeExpression>` **&lt;**
`VisualShaderNodeGroupBase<class_VisualShaderNodeGroupBase>` **&lt;**
`VisualShaderNodeResizableBase<class_VisualShaderNodeResizableBase>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A custom global visual shader graph expression written in Godot Shading
Language.

classref-introduction-group

## Description

Custom Godot Shader Language expression, which is placed on top of the
generated shader. You can place various function definitions inside to
call later in
`VisualShaderNodeExpression<class_VisualShaderNodeExpression>`s (which
are injected in the main shader functions). You can also declare
varyings, uniforms and global constants.
