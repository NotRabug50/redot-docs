github\_url  
hide

# XRFaceModifier3D

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A node for driving standard face meshes from
`XRFaceTracker<class_XRFaceTracker>` weights.

classref-introduction-group

## Description

This node applies weights from a `XRFaceTracker<class_XRFaceTracker>` to
a mesh with supporting face blend shapes.

The [Unified
Expressions](https://docs.vrcft.io/docs/tutorial-avatars/tutorial-avatars-extras/unified-blendshapes)
blend shapes are supported, as well as ARKit and SRanipal blend shapes.

The node attempts to identify blend shapes based on name matching. Blend
shapes should match the names listed in the [Unified Expressions
Compatibility](https://docs.vrcft.io/docs/tutorial-avatars/tutorial-avatars-extras/compatibility/overview)
chart.

classref-introduction-group

## Tutorials

-   `XR documentation index <../tutorials/xr/index>`

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`StringName<class_StringName>` **face\_tracker** =
`&"/user/face_tracker"`
`🔗<class_XRFaceModifier3D_property_face_tracker>`

classref-property-setget

-   `void (No return value.)` **set\_face\_tracker**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_face\_tracker**()

The `XRFaceTracker<class_XRFaceTracker>` path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **target** = `NodePath("")`
`🔗<class_XRFaceModifier3D_property_target>`

classref-property-setget

-   `void (No return value.)` **set\_target**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_target**()

The `NodePath<class_NodePath>` of the face
`MeshInstance3D<class_MeshInstance3D>`.
