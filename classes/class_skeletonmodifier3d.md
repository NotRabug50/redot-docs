github\_url  
hide

# SkeletonModifier3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`PhysicalBoneSimulator3D<class_PhysicalBoneSimulator3D>`,
`SkeletonIK3D<class_SkeletonIK3D>`,
`XRBodyModifier3D<class_XRBodyModifier3D>`,
`XRHandModifier3D<class_XRHandModifier3D>`

A Node that may modify Skeleton3D's bone.

classref-introduction-group

## Description

**SkeletonModifier3D** retrieves a target `Skeleton3D<class_Skeleton3D>`
by having a `Skeleton3D<class_Skeleton3D>` parent.

If there is `AnimationMixer<class_AnimationMixer>`, modification always
performs after playback process of the
`AnimationMixer<class_AnimationMixer>`.

This node should be used to implement custom IK solvers, constraints, or
skeleton physics.

classref-introduction-group

## Tutorials

-   [Design of the Skeleton Modifier
    3D](https://godotengine.org/article/design-of-the-skeleton-modifier-3d/)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**modification\_processed**()
`🔗<class_SkeletonModifier3D_signal_modification_processed>`

Notifies when the modification have been finished.

\*\*Note:\*\* If you want to get the modified bone pose by the modifier,
you must use
`Skeleton3D.get_bone_pose<class_Skeleton3D_method_get_bone_pose>` or
`Skeleton3D.get_bone_global_pose<class_Skeleton3D_method_get_bone_global_pose>`
at the moment this signal is fired.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **active** = `true`
`🔗<class_SkeletonModifier3D_property_active>`

classref-property-setget

-   `void (No return value.)` **set\_active**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_active**()

If `true`, the **SkeletonModifier3D** will be processing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **influence** = `1.0`
`🔗<class_SkeletonModifier3D_property_influence>`

classref-property-setget

-   `void (No return value.)` **set\_influence**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_influence**()

Sets the influence of the modification.

\*\*Note:\*\* This value is used by `Skeleton3D<class_Skeleton3D>` to
blend, so the **SkeletonModifier3D** should always apply only 100% of
the result without interpolation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_process\_modification**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_SkeletonModifier3D_private_method__process_modification>`

Override this virtual method to implement a custom skeleton modifier.
You should do things like get the `Skeleton3D<class_Skeleton3D>`'s
current pose and apply the pose here.

`_process_modification<class_SkeletonModifier3D_private_method__process_modification>`
must not apply `influence<class_SkeletonModifier3D_property_influence>`
to bone poses because the `Skeleton3D<class_Skeleton3D>` automatically
applies influence to all bone poses set by the modifier.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Skeleton3D<class_Skeleton3D>` **get\_skeleton**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModifier3D_method_get_skeleton>`

Get parent `Skeleton3D<class_Skeleton3D>` node if found.
