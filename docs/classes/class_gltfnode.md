github\_url  
hide

# GLTFNode

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

glTF node class.

classref-introduction-group

## Description

Represents a glTF node. glTF nodes may have names, transforms, children
(other glTF nodes), and more specialized properties (represented by
their own classes).

glTF nodes generally exist inside of `GLTFState<class_GLTFState>` which
represents all data of a glTF file. Most of GLTFNode's properties are
indices of other data in the glTF file. You can extend a glTF node with
additional properties by using
`get_additional_data<class_GLTFNode_method_get_additional_data>` and
`set_additional_data<class_GLTFNode_method_set_additional_data>`.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [glTF scene and node
    spec](https://github.com/KhronosGroup/glTF-Tutorials/blob/master/gltfTutorial/gltfTutorial_004_ScenesNodes.md%22)

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

`int<class_int>` **camera** = `-1` `🔗<class_GLTFNode_property_camera>`

classref-property-setget

-   `void (No return value.)` **set\_camera**(value: `int<class_int>`)
-   `int<class_int>` **get\_camera**()

If this glTF node is a camera, the index of the
`GLTFCamera<class_GLTFCamera>` in the `GLTFState<class_GLTFState>` that
describes the camera's properties. If -1, this node is not a camera.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedInt32Array<class_PackedInt32Array>` **children** =
`PackedInt32Array()` `🔗<class_GLTFNode_property_children>`

classref-property-setget

-   `void (No return value.)` **set\_children**(value:
    `PackedInt32Array<class_PackedInt32Array>`)
-   `PackedInt32Array<class_PackedInt32Array>` **get\_children**()

The indices of the child nodes in the `GLTFState<class_GLTFState>`. If
this glTF node has no children, this will be an empty array.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedInt32Array<class_PackedInt32Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **height** = `-1` `🔗<class_GLTFNode_property_height>`

classref-property-setget

-   `void (No return value.)` **set\_height**(value: `int<class_int>`)
-   `int<class_int>` **get\_height**()

How deep into the node hierarchy this node is. A root node will have a
height of 0, its children will have a height of 1, and so on. If -1, the
height has not been calculated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **light** = `-1` `🔗<class_GLTFNode_property_light>`

classref-property-setget

-   `void (No return value.)` **set\_light**(value: `int<class_int>`)
-   `int<class_int>` **get\_light**()

If this glTF node is a light, the index of the
`GLTFLight<class_GLTFLight>` in the `GLTFState<class_GLTFState>` that
describes the light's properties. If -1, this node is not a light.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **mesh** = `-1` `🔗<class_GLTFNode_property_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_mesh**(value: `int<class_int>`)
-   `int<class_int>` **get\_mesh**()

If this glTF node is a mesh, the index of the `GLTFMesh<class_GLTFMesh>`
in the `GLTFState<class_GLTFState>` that describes the mesh's
properties. If -1, this node is not a mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **original\_name** = `""`
`🔗<class_GLTFNode_property_original_name>`

classref-property-setget

-   `void (No return value.)` **set\_original\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_original\_name**()

The original name of the node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **parent** = `-1` `🔗<class_GLTFNode_property_parent>`

classref-property-setget

-   `void (No return value.)` **set\_parent**(value: `int<class_int>`)
-   `int<class_int>` **get\_parent**()

The index of the parent node in the `GLTFState<class_GLTFState>`. If -1,
this node is a root node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **position** = `Vector3(0, 0, 0)`
`🔗<class_GLTFNode_property_position>`

classref-property-setget

-   `void (No return value.)` **set\_position**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_position**()

The position of the glTF node relative to its parent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Quaternion<class_Quaternion>` **rotation** = `Quaternion(0, 0, 0, 1)`
`🔗<class_GLTFNode_property_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_rotation**(value:
    `Quaternion<class_Quaternion>`)
-   `Quaternion<class_Quaternion>` **get\_rotation**()

The rotation of the glTF node relative to its parent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **scale** = `Vector3(1, 1, 1)`
`🔗<class_GLTFNode_property_scale>`

classref-property-setget

-   `void (No return value.)` **set\_scale**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_scale**()

The scale of the glTF node relative to its parent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **skeleton** = `-1`
`🔗<class_GLTFNode_property_skeleton>`

classref-property-setget

-   `void (No return value.)` **set\_skeleton**(value: `int<class_int>`)
-   `int<class_int>` **get\_skeleton**()

If this glTF node has a skeleton, the index of the
`GLTFSkeleton<class_GLTFSkeleton>` in the `GLTFState<class_GLTFState>`
that describes the skeleton's properties. If -1, this node does not have
a skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **skin** = `-1` `🔗<class_GLTFNode_property_skin>`

classref-property-setget

-   `void (No return value.)` **set\_skin**(value: `int<class_int>`)
-   `int<class_int>` **get\_skin**()

If this glTF node has a skin, the index of the
`GLTFSkin<class_GLTFSkin>` in the `GLTFState<class_GLTFState>` that
describes the skin's properties. If -1, this node does not have a skin.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform3D<class_Transform3D>` **xform** =
`Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_GLTFNode_property_xform>`

classref-property-setget

-   `void (No return value.)` **set\_xform**(value:
    `Transform3D<class_Transform3D>`)
-   `Transform3D<class_Transform3D>` **get\_xform**()

The transform of the glTF node relative to its parent. This property is
usually unused since the position, rotation, and scale properties are
preferred.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **append\_child\_index**(child\_index:
`int<class_int>`) `🔗<class_GLTFNode_method_append_child_index>`

Appends the given child node index to the
`children<class_GLTFNode_property_children>` array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_additional\_data**(extension\_name:
`StringName<class_StringName>`)
`🔗<class_GLTFNode_method_get_additional_data>`

Gets additional arbitrary data in this **GLTFNode** instance. This can
be used to keep per-node state data in
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes, which is
important because they are stateless.

The argument should be the
`GLTFDocumentExtension<class_GLTFDocumentExtension>` name (does not have
to match the extension name in the glTF file), and the return value can
be anything you set. If nothing was set, the return value is null.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_additional\_data**(extension\_name:
`StringName<class_StringName>`, additional\_data:
`Variant<class_Variant>`)
`🔗<class_GLTFNode_method_set_additional_data>`

Sets additional arbitrary data in this **GLTFNode** instance. This can
be used to keep per-node state data in
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes, which is
important because they are stateless.

The first argument should be the
`GLTFDocumentExtension<class_GLTFDocumentExtension>` name (does not have
to match the extension name in the glTF file), and the second argument
can be anything you want.
