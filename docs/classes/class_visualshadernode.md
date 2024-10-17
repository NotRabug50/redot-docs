github\_url  
hide

# VisualShaderNode

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeBillboard<class_VisualShaderNodeBillboard>`,
`VisualShaderNodeClamp<class_VisualShaderNodeClamp>`,
`VisualShaderNodeColorFunc<class_VisualShaderNodeColorFunc>`,
`VisualShaderNodeColorOp<class_VisualShaderNodeColorOp>`,
`VisualShaderNodeCompare<class_VisualShaderNodeCompare>`,
`VisualShaderNodeConstant<class_VisualShaderNodeConstant>`,
`VisualShaderNodeCubemap<class_VisualShaderNodeCubemap>`,
`VisualShaderNodeCustom<class_VisualShaderNodeCustom>`,
`VisualShaderNodeDerivativeFunc<class_VisualShaderNodeDerivativeFunc>`,
`VisualShaderNodeDeterminant<class_VisualShaderNodeDeterminant>`,
`VisualShaderNodeDistanceFade<class_VisualShaderNodeDistanceFade>`,
`VisualShaderNodeDotProduct<class_VisualShaderNodeDotProduct>`,
`VisualShaderNodeFloatFunc<class_VisualShaderNodeFloatFunc>`,
`VisualShaderNodeFloatOp<class_VisualShaderNodeFloatOp>`,
`VisualShaderNodeFresnel<class_VisualShaderNodeFresnel>`,
`VisualShaderNodeIf<class_VisualShaderNodeIf>`,
`VisualShaderNodeInput<class_VisualShaderNodeInput>`,
`VisualShaderNodeIntFunc<class_VisualShaderNodeIntFunc>`,
`VisualShaderNodeIntOp<class_VisualShaderNodeIntOp>`,
`VisualShaderNodeIs<class_VisualShaderNodeIs>`,
`VisualShaderNodeLinearSceneDepth<class_VisualShaderNodeLinearSceneDepth>`,
`VisualShaderNodeMix<class_VisualShaderNodeMix>`,
`VisualShaderNodeMultiplyAdd<class_VisualShaderNodeMultiplyAdd>`,
`VisualShaderNodeOuterProduct<class_VisualShaderNodeOuterProduct>`,
`VisualShaderNodeOutput<class_VisualShaderNodeOutput>`,
`VisualShaderNodeParameter<class_VisualShaderNodeParameter>`,
`VisualShaderNodeParameterRef<class_VisualShaderNodeParameterRef>`,
`VisualShaderNodeParticleAccelerator<class_VisualShaderNodeParticleAccelerator>`,
`VisualShaderNodeParticleConeVelocity<class_VisualShaderNodeParticleConeVelocity>`,
`VisualShaderNodeParticleEmit<class_VisualShaderNodeParticleEmit>`,
`VisualShaderNodeParticleEmitter<class_VisualShaderNodeParticleEmitter>`,
`VisualShaderNodeParticleMultiplyByAxisAngle<class_VisualShaderNodeParticleMultiplyByAxisAngle>`,
`VisualShaderNodeParticleRandomness<class_VisualShaderNodeParticleRandomness>`,
`VisualShaderNodeProximityFade<class_VisualShaderNodeProximityFade>`,
`VisualShaderNodeRandomRange<class_VisualShaderNodeRandomRange>`,
`VisualShaderNodeRemap<class_VisualShaderNodeRemap>`,
`VisualShaderNodeReroute<class_VisualShaderNodeReroute>`,
`VisualShaderNodeResizableBase<class_VisualShaderNodeResizableBase>`,
`VisualShaderNodeRotationByAxis<class_VisualShaderNodeRotationByAxis>`,
`VisualShaderNodeSample3D<class_VisualShaderNodeSample3D>`,
`VisualShaderNodeScreenNormalWorldSpace<class_VisualShaderNodeScreenNormalWorldSpace>`,
`VisualShaderNodeScreenUVToSDF<class_VisualShaderNodeScreenUVToSDF>`,
`VisualShaderNodeSDFRaymarch<class_VisualShaderNodeSDFRaymarch>`,
`VisualShaderNodeSDFToScreenUV<class_VisualShaderNodeSDFToScreenUV>`,
`VisualShaderNodeSmoothStep<class_VisualShaderNodeSmoothStep>`,
`VisualShaderNodeStep<class_VisualShaderNodeStep>`,
`VisualShaderNodeSwitch<class_VisualShaderNodeSwitch>`,
`VisualShaderNodeTexture<class_VisualShaderNodeTexture>`,
`VisualShaderNodeTextureSDF<class_VisualShaderNodeTextureSDF>`,
`VisualShaderNodeTextureSDFNormal<class_VisualShaderNodeTextureSDFNormal>`,
`VisualShaderNodeTransformCompose<class_VisualShaderNodeTransformCompose>`,
`VisualShaderNodeTransformDecompose<class_VisualShaderNodeTransformDecompose>`,
`VisualShaderNodeTransformFunc<class_VisualShaderNodeTransformFunc>`,
`VisualShaderNodeTransformOp<class_VisualShaderNodeTransformOp>`,
`VisualShaderNodeTransformVecMult<class_VisualShaderNodeTransformVecMult>`,
`VisualShaderNodeUIntFunc<class_VisualShaderNodeUIntFunc>`,
`VisualShaderNodeUIntOp<class_VisualShaderNodeUIntOp>`,
`VisualShaderNodeUVFunc<class_VisualShaderNodeUVFunc>`,
`VisualShaderNodeUVPolarCoord<class_VisualShaderNodeUVPolarCoord>`,
`VisualShaderNodeVarying<class_VisualShaderNodeVarying>`,
`VisualShaderNodeVectorBase<class_VisualShaderNodeVectorBase>`,
`VisualShaderNodeWorldPositionFromDepth<class_VisualShaderNodeWorldPositionFromDepth>`

Base class for `VisualShader<class_VisualShader>` nodes. Not related to
scene nodes.

classref-introduction-group

## Description

Visual shader graphs consist of various nodes. Each node in the graph is
a separate object and they are represented as a rectangular boxes with
title and a set of properties. Each node also has connection ports that
allow to connect it to another nodes and control the flow of the shader.

classref-introduction-group

## Tutorials

-   `Using VisualShaders <../tutorials/shaders/visual_shaders>`

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **PortType**: `🔗<enum_VisualShaderNode_PortType>`

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_SCALAR** = `0`

Floating-point scalar. Translated to `float` type in shader code.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_SCALAR\_INT** =
`1`

Integer scalar. Translated to `int` type in shader code.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_SCALAR\_UINT**
= `2`

Unsigned integer scalar. Translated to `uint` type in shader code.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_VECTOR\_2D** =
`3`

2D vector of floating-point values. Translated to `vec2` type in shader
code.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_VECTOR\_3D** =
`4`

3D vector of floating-point values. Translated to `vec3` type in shader
code.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_VECTOR\_4D** =
`5`

4D vector of floating-point values. Translated to `vec4` type in shader
code.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_BOOLEAN** = `6`

Boolean type. Translated to `bool` type in shader code.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_TRANSFORM** =
`7`

Transform type. Translated to `mat4` type in shader code.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_SAMPLER** = `8`

Sampler type. Translated to reference of sampler uniform in shader code.
Can only be used for input ports in non-uniform nodes.

classref-enumeration-constant

`PortType<enum_VisualShaderNode_PortType>` **PORT\_TYPE\_MAX** = `9`

Represents the size of the `PortType<enum_VisualShaderNode_PortType>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **linked\_parent\_graph\_frame** = `-1`
`🔗<class_VisualShaderNode_property_linked_parent_graph_frame>`

classref-property-setget

-   `void (No return value.)` **set\_frame**(value: `int<class_int>`)
-   `int<class_int>` **get\_frame**()

Represents the index of the frame this node is linked to. If set to `-1`
the node is not linked to any frame.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **output\_port\_for\_preview** = `-1`
`🔗<class_VisualShaderNode_property_output_port_for_preview>`

classref-property-setget

-   `void (No return value.)` **set\_output\_port\_for\_preview**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_output\_port\_for\_preview**()

Sets the output port index which will be showed for preview. If set to
`-1` no port will be open for preview.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear\_default\_input\_values**()
`🔗<class_VisualShaderNode_method_clear_default_input_values>`

Clears the default input ports value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_default\_input\_port**(type:
`PortType<enum_VisualShaderNode_PortType>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNode_method_get_default_input_port>`

Returns the input port which should be connected by default when this
node is created as a result of dragging a connection from an existing
node to the empty space on the graph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_default\_input\_values**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNode_method_get_default_input_values>`

Returns an `Array<class_Array>` containing default values for all of the
input ports of the node in the form
`[index0, value0, index1, value1, ...]`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_input\_port\_default\_value**(port:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNode_method_get_input_port_default_value>`

Returns the default value of the input `port`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_input\_port\_default\_value**(port:
`int<class_int>`)
`🔗<class_VisualShaderNode_method_remove_input_port_default_value>`

Removes the default value of the input `port`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_default\_input\_values**(values:
`Array<class_Array>`)
`🔗<class_VisualShaderNode_method_set_default_input_values>`

Sets the default input ports values using an `Array<class_Array>` of the
form `[index0, value0, index1, value1, ...]`. For example:
`[0, Vector3(0, 0, 0), 1, Vector3(0, 0, 0)]`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_input\_port\_default\_value**(port:
`int<class_int>`, value: `Variant<class_Variant>`, prev\_value:
`Variant<class_Variant>` = null)
`🔗<class_VisualShaderNode_method_set_input_port_default_value>`

Sets the default `value` for the selected input `port`.
