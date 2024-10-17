github\_url  
hide

# SubViewportContainer

**Inherits:** `Container<class_Container>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A container used for displaying the contents of a
`SubViewport<class_SubViewport>`.

classref-introduction-group

## Description

A container that displays the contents of underlying
`SubViewport<class_SubViewport>` child nodes. It uses the combined size
of the `SubViewport<class_SubViewport>`s as minimum size, unless
`stretch<class_SubViewportContainer_property_stretch>` is enabled.

\*\*Note:\*\* Changing a **SubViewportContainer**'s
`Control.scale<class_Control_property_scale>` will cause its contents to
appear distorted. To change its visual size without causing distortion,
adjust the node's margins instead (if it's not already in a container).

\*\*Note:\*\* The **SubViewportContainer** forwards mouse-enter and
mouse-exit notifications to its sub-viewports.

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
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **stretch** = `false`
`🔗<class_SubViewportContainer_property_stretch>`

classref-property-setget

-   `void (No return value.)` **set\_stretch**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_stretch\_enabled**()

If `true`, the sub-viewport will be automatically resized to the
control's size.

\*\*Note:\*\* If `true`, this will prohibit changing
`SubViewport.size<class_SubViewport_property_size>` of its children
manually.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **stretch\_shrink** = `1`
`🔗<class_SubViewportContainer_property_stretch_shrink>`

classref-property-setget

-   `void (No return value.)` **set\_stretch\_shrink**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_stretch\_shrink**()

Divides the sub-viewport's effective resolution by this value while
preserving its scale. This can be used to speed up rendering.

For example, a 1280×720 sub-viewport with
`stretch_shrink<class_SubViewportContainer_property_stretch_shrink>` set
to `2` will be rendered at 640×360 while occupying the same size in the
container.

\*\*Note:\*\* `stretch<class_SubViewportContainer_property_stretch>`
must be `true` for this property to work.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_propagate\_input\_event**(event:
`InputEvent<class_InputEvent>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SubViewportContainer_private_method__propagate_input_event>`

**Experimental:** This method may be changed or removed in future
versions.

Virtual method to be implemented by the user. If it returns `true`, the
`event` is propagated to `SubViewport<class_SubViewport>` children.
Propagation doesn't happen if it returns `false`. If the function is not
implemented, all events are propagated to SubViewports.
