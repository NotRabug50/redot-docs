github\_url  
hide

# GLTFPhysicsShape

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a glTF physics shape.

classref-introduction-group

## Description

Represents a physics shape as defined by the `OMI_physics_shape` or
`OMI_collider` glTF extensions. This class is an intermediary between
the glTF data and Godot's nodes, and it's abstracted in a way that
allows adding support for different glTF physics extensions in the
future.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [OMI\_physics\_shape glTF
    extension](https://github.com/omigroup/gltf-extensions/tree/main/extensions/2.0/OMI_physics_shape)
-   [OMI\_collider glTF
    extension](https://github.com/omigroup/gltf-extensions/tree/main/extensions/2.0/Archived/OMI_collider)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **height** = `2.0`
`🔗<class_GLTFPhysicsShape_property_height>`

classref-property-setget

-   `void (No return value.)` **set\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_height**()

The height of the shape, in meters. This is only used when the shape
type is "capsule" or "cylinder". This value should not be negative, and
for "capsule" it should be at least twice the radius.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ImporterMesh<class_ImporterMesh>` **importer\_mesh**
`🔗<class_GLTFPhysicsShape_property_importer_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_importer\_mesh**(value:
    `ImporterMesh<class_ImporterMesh>`)
-   `ImporterMesh<class_ImporterMesh>` **get\_importer\_mesh**()

The `ImporterMesh<class_ImporterMesh>` resource of the shape. This is
only used when the shape type is "hull" (convex hull) or "trimesh"
(concave trimesh).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **is\_trigger** = `false`
`🔗<class_GLTFPhysicsShape_property_is_trigger>`

classref-property-setget

-   `void (No return value.)` **set\_is\_trigger**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_is\_trigger**()

If `true`, indicates that this shape is a trigger. For Godot, this means
that the shape should be a child of an Area3D node.

This is the only variable not used in the
`to_node<class_GLTFPhysicsShape_method_to_node>` method, it's intended
to be used alongside when deciding where to add the generated node as a
child.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **mesh\_index** = `-1`
`🔗<class_GLTFPhysicsShape_property_mesh_index>`

classref-property-setget

-   `void (No return value.)` **set\_mesh\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_mesh\_index**()

The index of the shape's mesh in the glTF file. This is only used when
the shape type is "hull" (convex hull) or "trimesh" (concave trimesh).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radius** = `0.5`
`🔗<class_GLTFPhysicsShape_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The radius of the shape, in meters. This is only used when the shape
type is "capsule", "cylinder", or "sphere". This value should not be
negative.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **shape\_type** = `""`
`🔗<class_GLTFPhysicsShape_property_shape_type>`

classref-property-setget

-   `void (No return value.)` **set\_shape\_type**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_shape\_type**()

The type of shape this shape represents. Valid values are "box",
"capsule", "cylinder", "sphere", "hull", and "trimesh".

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **size** = `Vector3(1, 1, 1)`
`🔗<class_GLTFPhysicsShape_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_size**()

The size of the shape, in meters. This is only used when the shape type
is "box", and it represents the "diameter" of the box. This value should
not be negative.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`GLTFPhysicsShape<class_GLTFPhysicsShape>`
**from\_dictionary**(dictionary: `Dictionary<class_Dictionary>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFPhysicsShape_method_from_dictionary>`

Creates a new GLTFPhysicsShape instance by parsing the given
`Dictionary<class_Dictionary>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GLTFPhysicsShape<class_GLTFPhysicsShape>` **from\_node**(shape\_node:
`CollisionShape3D<class_CollisionShape3D>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFPhysicsShape_method_from_node>`

Creates a new GLTFPhysicsShape instance from the given Godot
`CollisionShape3D<class_CollisionShape3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GLTFPhysicsShape<class_GLTFPhysicsShape>`
**from\_resource**(shape\_resource: `Shape3D<class_Shape3D>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFPhysicsShape_method_from_resource>`

Creates a new GLTFPhysicsShape instance from the given Godot
`Shape3D<class_Shape3D>` resource.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **to\_dictionary**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GLTFPhysicsShape_method_to_dictionary>`

Serializes this GLTFPhysicsShape instance into a
`Dictionary<class_Dictionary>` in the format defined by
`OMI_physics_shape`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CollisionShape3D<class_CollisionShape3D>` **to\_node**(cache\_shapes:
`bool<class_bool>` = false) `🔗<class_GLTFPhysicsShape_method_to_node>`

Converts this GLTFPhysicsShape instance into a Godot
`CollisionShape3D<class_CollisionShape3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Shape3D<class_Shape3D>` **to\_resource**(cache\_shapes:
`bool<class_bool>` = false)
`🔗<class_GLTFPhysicsShape_method_to_resource>`

Converts this GLTFPhysicsShape instance into a Godot
`Shape3D<class_Shape3D>` resource.
