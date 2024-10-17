github\_url  
hide

# PhysicsServer3DRenderingServerHandler

**Inherits:** `Object<class_Object>`

A class used to provide
`PhysicsServer3DExtension._soft_body_update_rendering_server<class_PhysicsServer3DExtension_private_method__soft_body_update_rendering_server>`
with a rendering handler for soft bodies.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_set\_aabb**(aabb: `AABB<class_AABB>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer3DRenderingServerHandler_private_method__set_aabb>`

Called by the `PhysicsServer3D<class_PhysicsServer3D>` to set the
bounding box for the `SoftBody3D<class_SoftBody3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_normal**(vertex\_id:
`int<class_int>`, normal: `Vector3<class_Vector3>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer3DRenderingServerHandler_private_method__set_normal>`

Called by the `PhysicsServer3D<class_PhysicsServer3D>` to set the normal
for the `SoftBody3D<class_SoftBody3D>` vertex at the index specified by
`vertex_id`.

\*\*Note:\*\* The `normal` parameter used to be of type `const void*`
prior to Godot 4.2.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_vertex**(vertex\_id:
`int<class_int>`, vertex: `Vector3<class_Vector3>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer3DRenderingServerHandler_private_method__set_vertex>`

Called by the `PhysicsServer3D<class_PhysicsServer3D>` to set the
position for the `SoftBody3D<class_SoftBody3D>` vertex at the index
specified by `vertex_id`.

\*\*Note:\*\* The `vertex` parameter used to be of type `const void*`
prior to Godot 4.2.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_aabb**(aabb: `AABB<class_AABB>`)
`🔗<class_PhysicsServer3DRenderingServerHandler_method_set_aabb>`

Sets the bounding box for the `SoftBody3D<class_SoftBody3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_normal**(vertex\_id: `int<class_int>`,
normal: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3DRenderingServerHandler_method_set_normal>`

Sets the normal for the `SoftBody3D<class_SoftBody3D>` vertex at the
index specified by `vertex_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_vertex**(vertex\_id: `int<class_int>`,
vertex: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3DRenderingServerHandler_method_set_vertex>`

Sets the position for the `SoftBody3D<class_SoftBody3D>` vertex at the
index specified by `vertex_id`.
