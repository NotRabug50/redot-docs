github\_url  
hide

# RemoteTransform3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

RemoteTransform3D pushes its own `Transform3D<class_Transform3D>` to
another `Node3D<class_Node3D>` derived Node in the scene.

classref-introduction-group

## Description

RemoteTransform3D pushes its own `Transform3D<class_Transform3D>` to
another `Node3D<class_Node3D>` derived Node (called the remote node) in
the scene.

It can be set to update another Node's position, rotation and/or scale.
It can use either global or local coordinates.

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

`NodePath<class_NodePath>` **remote\_path** = `NodePath("")`
`🔗<class_RemoteTransform3D_property_remote_path>`

classref-property-setget

-   `void (No return value.)` **set\_remote\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_remote\_node**()

The `NodePath<class_NodePath>` to the remote node, relative to the
RemoteTransform3D's position in the scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **update\_position** = `true`
`🔗<class_RemoteTransform3D_property_update_position>`

classref-property-setget

-   `void (No return value.)` **set\_update\_position**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_update\_position**()

If `true`, the remote node's position is updated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **update\_rotation** = `true`
`🔗<class_RemoteTransform3D_property_update_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_update\_rotation**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_update\_rotation**()

If `true`, the remote node's rotation is updated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **update\_scale** = `true`
`🔗<class_RemoteTransform3D_property_update_scale>`

classref-property-setget

-   `void (No return value.)` **set\_update\_scale**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_update\_scale**()

If `true`, the remote node's scale is updated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_global\_coordinates** = `true`
`🔗<class_RemoteTransform3D_property_use_global_coordinates>`

classref-property-setget

-   `void (No return value.)` **set\_use\_global\_coordinates**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_global\_coordinates**()

If `true`, global coordinates are used. If `false`, local coordinates
are used.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **force\_update\_cache**()
`🔗<class_RemoteTransform3D_method_force_update_cache>`

**RemoteTransform3D** caches the remote node. It may not notice if the
remote node disappears;
`force_update_cache<class_RemoteTransform3D_method_force_update_cache>`
forces it to update the cache again.
