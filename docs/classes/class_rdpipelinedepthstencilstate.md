github\_url  
hide

# RDPipelineDepthStencilState

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Pipeline depth/stencil state (used by
`RenderingDevice<class_RenderingDevice>`).

classref-introduction-group

## Description

**RDPipelineDepthStencilState** controls the way depth and stencil
comparisons are performed when sampling those values using
`RenderingDevice<class_RenderingDevice>`.

classref-reftable-group

## Properties

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

## Property Descriptions

classref-property

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**back\_op\_compare** = `7`
`🔗<class_RDPipelineDepthStencilState_property_back_op_compare>`

classref-property-setget

-   `void (No return value.)` **set\_back\_op\_compare**(value:
    `CompareOperator<enum_RenderingDevice_CompareOperator>`)
-   `CompareOperator<enum_RenderingDevice_CompareOperator>`
    **get\_back\_op\_compare**()

The method used for comparing the previous back stencil value and
`back_op_reference<class_RDPipelineDepthStencilState_property_back_op_reference>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **back\_op\_compare\_mask** = `0`
`🔗<class_RDPipelineDepthStencilState_property_back_op_compare_mask>`

classref-property-setget

-   `void (No return value.)` **set\_back\_op\_compare\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_back\_op\_compare\_mask**()

Selects which bits from the back stencil value will be compared.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**back\_op\_depth\_fail** = `1`
`🔗<class_RDPipelineDepthStencilState_property_back_op_depth_fail>`

classref-property-setget

-   `void (No return value.)` **set\_back\_op\_depth\_fail**(value:
    `StencilOperation<enum_RenderingDevice_StencilOperation>`)
-   `StencilOperation<enum_RenderingDevice_StencilOperation>`
    **get\_back\_op\_depth\_fail**()

The operation to perform on the stencil buffer for back pixels that pass
the stencil test but fail the depth test.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**back\_op\_fail** = `1`
`🔗<class_RDPipelineDepthStencilState_property_back_op_fail>`

classref-property-setget

-   `void (No return value.)` **set\_back\_op\_fail**(value:
    `StencilOperation<enum_RenderingDevice_StencilOperation>`)
-   `StencilOperation<enum_RenderingDevice_StencilOperation>`
    **get\_back\_op\_fail**()

The operation to perform on the stencil buffer for back pixels that fail
the stencil test.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**back\_op\_pass** = `1`
`🔗<class_RDPipelineDepthStencilState_property_back_op_pass>`

classref-property-setget

-   `void (No return value.)` **set\_back\_op\_pass**(value:
    `StencilOperation<enum_RenderingDevice_StencilOperation>`)
-   `StencilOperation<enum_RenderingDevice_StencilOperation>`
    **get\_back\_op\_pass**()

The operation to perform on the stencil buffer for back pixels that pass
the stencil test.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **back\_op\_reference** = `0`
`🔗<class_RDPipelineDepthStencilState_property_back_op_reference>`

classref-property-setget

-   `void (No return value.)` **set\_back\_op\_reference**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_back\_op\_reference**()

The value the previous back stencil value will be compared to.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **back\_op\_write\_mask** = `0`
`🔗<class_RDPipelineDepthStencilState_property_back_op_write_mask>`

classref-property-setget

-   `void (No return value.)` **set\_back\_op\_write\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_back\_op\_write\_mask**()

Selects which bits from the back stencil value will be changed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**depth\_compare\_operator** = `7`
`🔗<class_RDPipelineDepthStencilState_property_depth_compare_operator>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_compare\_operator**(value:
    `CompareOperator<enum_RenderingDevice_CompareOperator>`)
-   `CompareOperator<enum_RenderingDevice_CompareOperator>`
    **get\_depth\_compare\_operator**()

The method used for comparing the previous and current depth values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **depth\_range\_max** = `0.0`
`🔗<class_RDPipelineDepthStencilState_property_depth_range_max>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_range\_max**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth\_range\_max**()

The maximum depth that returns true for
`enable_depth_range<class_RDPipelineDepthStencilState_property_enable_depth_range>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **depth\_range\_min** = `0.0`
`🔗<class_RDPipelineDepthStencilState_property_depth_range_min>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_range\_min**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth\_range\_min**()

The minimum depth that returns true for
`enable_depth_range<class_RDPipelineDepthStencilState_property_enable_depth_range>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_depth\_range** = `false`
`🔗<class_RDPipelineDepthStencilState_property_enable_depth_range>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_depth\_range**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_depth\_range**()

If `true`, each depth value will be tested to see if it is between
`depth_range_min<class_RDPipelineDepthStencilState_property_depth_range_min>`
and
`depth_range_max<class_RDPipelineDepthStencilState_property_depth_range_max>`.
If it is outside of these values, it is discarded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_depth\_test** = `false`
`🔗<class_RDPipelineDepthStencilState_property_enable_depth_test>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_depth\_test**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_depth\_test**()

If `true`, enables depth testing which allows objects to be
automatically occluded by other objects based on their depth. This also
allows objects to be partially occluded by other objects. If `false`,
objects will appear in the order they were drawn (like in Godot's 2D
renderer).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_depth\_write** = `false`
`🔗<class_RDPipelineDepthStencilState_property_enable_depth_write>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_depth\_write**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_depth\_write**()

If `true`, writes to the depth buffer whenever the depth test returns
true. Only works when enable\_depth\_test is also true.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_stencil** = `false`
`🔗<class_RDPipelineDepthStencilState_property_enable_stencil>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_stencil**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_stencil**()

If `true`, enables stencil testing. There are separate stencil buffers
for front-facing triangles and back-facing triangles. See properties
that begin with "front\_op" and properties with "back\_op" for each.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CompareOperator<enum_RenderingDevice_CompareOperator>`
**front\_op\_compare** = `7`
`🔗<class_RDPipelineDepthStencilState_property_front_op_compare>`

classref-property-setget

-   `void (No return value.)` **set\_front\_op\_compare**(value:
    `CompareOperator<enum_RenderingDevice_CompareOperator>`)
-   `CompareOperator<enum_RenderingDevice_CompareOperator>`
    **get\_front\_op\_compare**()

The method used for comparing the previous front stencil value and
`front_op_reference<class_RDPipelineDepthStencilState_property_front_op_reference>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **front\_op\_compare\_mask** = `0`
`🔗<class_RDPipelineDepthStencilState_property_front_op_compare_mask>`

classref-property-setget

-   `void (No return value.)` **set\_front\_op\_compare\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_front\_op\_compare\_mask**()

Selects which bits from the front stencil value will be compared.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**front\_op\_depth\_fail** = `1`
`🔗<class_RDPipelineDepthStencilState_property_front_op_depth_fail>`

classref-property-setget

-   `void (No return value.)` **set\_front\_op\_depth\_fail**(value:
    `StencilOperation<enum_RenderingDevice_StencilOperation>`)
-   `StencilOperation<enum_RenderingDevice_StencilOperation>`
    **get\_front\_op\_depth\_fail**()

The operation to perform on the stencil buffer for front pixels that
pass the stencil test but fail the depth test.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**front\_op\_fail** = `1`
`🔗<class_RDPipelineDepthStencilState_property_front_op_fail>`

classref-property-setget

-   `void (No return value.)` **set\_front\_op\_fail**(value:
    `StencilOperation<enum_RenderingDevice_StencilOperation>`)
-   `StencilOperation<enum_RenderingDevice_StencilOperation>`
    **get\_front\_op\_fail**()

The operation to perform on the stencil buffer for front pixels that
fail the stencil test.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StencilOperation<enum_RenderingDevice_StencilOperation>`
**front\_op\_pass** = `1`
`🔗<class_RDPipelineDepthStencilState_property_front_op_pass>`

classref-property-setget

-   `void (No return value.)` **set\_front\_op\_pass**(value:
    `StencilOperation<enum_RenderingDevice_StencilOperation>`)
-   `StencilOperation<enum_RenderingDevice_StencilOperation>`
    **get\_front\_op\_pass**()

The operation to perform on the stencil buffer for front pixels that
pass the stencil test.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **front\_op\_reference** = `0`
`🔗<class_RDPipelineDepthStencilState_property_front_op_reference>`

classref-property-setget

-   `void (No return value.)` **set\_front\_op\_reference**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_front\_op\_reference**()

The value the previous front stencil value will be compared to.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **front\_op\_write\_mask** = `0`
`🔗<class_RDPipelineDepthStencilState_property_front_op_write_mask>`

classref-property-setget

-   `void (No return value.)` **set\_front\_op\_write\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_front\_op\_write\_mask**()

Selects which bits from the front stencil value will be changed.
