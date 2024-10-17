github\_url  
hide

# OpenXRCompositionLayer

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`OpenXRCompositionLayerCylinder<class_OpenXRCompositionLayerCylinder>`,
`OpenXRCompositionLayerEquirect<class_OpenXRCompositionLayerEquirect>`,
`OpenXRCompositionLayerQuad<class_OpenXRCompositionLayerQuad>`

The parent class of all OpenXR composition layer nodes.

classref-introduction-group

## Description

Composition layers allow 2D viewports to be displayed inside of the
headset by the XR compositor through special projections that retain
their quality. This allows for rendering clear text while keeping the
layer at a native resolution.

\*\*Note:\*\* If the OpenXR runtime doesn't support the given
composition layer type, a fallback mesh can be generated with a
`ViewportTexture<class_ViewportTexture>`, in order to emulate the
composition layer.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **alpha\_blend** = `false`
`🔗<class_OpenXRCompositionLayer_property_alpha_blend>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_blend**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_alpha\_blend**()

Enables the blending the layer using its alpha channel.

Can be combined with
`Viewport.transparent_bg<class_Viewport_property_transparent_bg>` to
give the layer a transparent background.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **android\_surface\_size** =
`Vector2i(1024, 1024)`
`🔗<class_OpenXRCompositionLayer_property_android_surface_size>`

classref-property-setget

-   `void (No return value.)` **set\_android\_surface\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_android\_surface\_size**()

The size of the Android surface to create if
`use_android_surface<class_OpenXRCompositionLayer_property_use_android_surface>`
is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_hole\_punch** = `false`
`🔗<class_OpenXRCompositionLayer_property_enable_hole_punch>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_hole\_punch**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_hole\_punch**()

Enables a technique called "hole punching", which allows putting the
composition layer behind the main projection layer (i.e. setting
`sort_order<class_OpenXRCompositionLayer_property_sort_order>` to a
negative value) while "punching a hole" through everything rendered by
Godot so that the layer is still visible.

This can be used to create the illusion that the composition layer
exists in the same 3D space as everything rendered by Godot, allowing
objects to appear to pass both behind or in front of the composition
layer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SubViewport<class_SubViewport>` **layer\_viewport**
`🔗<class_OpenXRCompositionLayer_property_layer_viewport>`

classref-property-setget

-   `void (No return value.)` **set\_layer\_viewport**(value:
    `SubViewport<class_SubViewport>`)
-   `SubViewport<class_SubViewport>` **get\_layer\_viewport**()

The `SubViewport<class_SubViewport>` to render on the composition layer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sort\_order** = `1`
`🔗<class_OpenXRCompositionLayer_property_sort_order>`

classref-property-setget

-   `void (No return value.)` **set\_sort\_order**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_sort\_order**()

The sort order for this composition layer. Higher numbers will be shown
in front of lower numbers.

\*\*Note:\*\* This will have no effect if a fallback mesh is being used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_android\_surface** = `false`
`🔗<class_OpenXRCompositionLayer_property_use_android_surface>`

classref-property-setget

-   `void (No return value.)` **set\_use\_android\_surface**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_android\_surface**()

If enabled, an Android surface will be created (with the dimensions from
`android_surface_size<class_OpenXRCompositionLayer_property_android_surface_size>`)
which will provide the 2D content for the composition layer, rather than
using
`layer_viewport<class_OpenXRCompositionLayer_property_layer_viewport>`.

See
`get_android_surface<class_OpenXRCompositionLayer_method_get_android_surface>`
for information about how to get the surface so that your application
can draw to it.

\*\*Note:\*\* This will only work in Android builds.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`JavaObject<class_JavaObject>` **get\_android\_surface**()
`🔗<class_OpenXRCompositionLayer_method_get_android_surface>`

Returns a `JavaObject<class_JavaObject>` representing an
`android.view.Surface` if
`use_android_surface<class_OpenXRCompositionLayer_property_use_android_surface>`
is enabled and OpenXR has created the surface. Otherwise, this will
return `null`.

\*\*Note:\*\* The surface can only be created during an active OpenXR
session. So, if
`use_android_surface<class_OpenXRCompositionLayer_property_use_android_surface>`
is enabled outside of an OpenXR session, it won't be created until a new
session fully starts.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **intersects\_ray**(origin:
`Vector3<class_Vector3>`, direction: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRCompositionLayer_method_intersects_ray>`

Returns UV coordinates where the given ray intersects with the
composition layer. `origin` and `direction` must be in global space.

Returns `Vector2(-1.0, -1.0)` if the ray doesn't intersect.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_natively\_supported**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRCompositionLayer_method_is_natively_supported>`

Returns true if the OpenXR runtime natively supports this composition
layer type.

\*\*Note:\*\* This will only return an accurate result after the OpenXR
session has started.
