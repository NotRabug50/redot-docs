github\_url  
hide

# GLTFPhysicsBody

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a glTF physics body.

classref-introduction-group

## Description

Represents a physics body as an intermediary between the
`OMI_physics_body` glTF data and Godot's nodes, and it's abstracted in a
way that allows adding support for different glTF physics extensions in
the future.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [OMI\_physics\_body glTF
    extension](https://github.com/omigroup/gltf-extensions/tree/main/extensions/2.0/OMI_physics_body)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector3<class_Vector3>` **angular\_velocity** = `Vector3(0, 0, 0)`
`🔗<class_GLTFPhysicsBody_property_angular_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_angular\_velocity**()

The angular velocity of the physics body, in radians per second. This is
only used when the body type is "rigid" or "vehicle".

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **body\_type** = `"rigid"`
`🔗<class_GLTFPhysicsBody_property_body_type>`

classref-property-setget

-   `void (No return value.)` **set\_body\_type**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_body\_type**()

The type of the body. When importing, this controls what type of
`CollisionObject3D<class_CollisionObject3D>` node Godot should generate.
Valid values are "static", "animatable", "character", "rigid",
"vehicle", and "trigger". When exporting, this will be squashed down to
one of "static", "kinematic", or "dynamic" motion types, or the
"trigger" property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **center\_of\_mass** = `Vector3(0, 0, 0)`
`🔗<class_GLTFPhysicsBody_property_center_of_mass>`

classref-property-setget

-   `void (No return value.)` **set\_center\_of\_mass**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_center\_of\_mass**()

The center of mass of the body, in meters. This is in local space
relative to the body. By default, the center of the mass is the body's
origin.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **inertia\_diagonal** = `Vector3(0, 0, 0)`
`🔗<class_GLTFPhysicsBody_property_inertia_diagonal>`

classref-property-setget

-   `void (No return value.)` **set\_inertia\_diagonal**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_inertia\_diagonal**()

The inertia strength of the physics body, in kilogram meter squared
(kg⋅m²). This represents the inertia around the principle axes, the
diagonal of the inertia tensor matrix. This is only used when the body
type is "rigid" or "vehicle".

When converted to a Godot `RigidBody3D<class_RigidBody3D>` node, if this
value is zero, then the inertia will be calculated automatically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Quaternion<class_Quaternion>` **inertia\_orientation** =
`Quaternion(0, 0, 0, 1)`
`🔗<class_GLTFPhysicsBody_property_inertia_orientation>`

classref-property-setget

-   `void (No return value.)` **set\_inertia\_orientation**(value:
    `Quaternion<class_Quaternion>`)
-   `Quaternion<class_Quaternion>` **get\_inertia\_orientation**()

The inertia orientation of the physics body. This defines the rotation
of the inertia's principle axes relative to the object's local axes.
This is only used when the body type is "rigid" or "vehicle" and
`inertia_diagonal<class_GLTFPhysicsBody_property_inertia_diagonal>` is
set to a non-zero value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Basis<class_Basis>` **inertia\_tensor** =
`Basis(0, 0, 0, 0, 0, 0, 0, 0, 0)`
`🔗<class_GLTFPhysicsBody_property_inertia_tensor>`

classref-property-setget

-   `void (No return value.)` **set\_inertia\_tensor**(value:
    `Basis<class_Basis>`)
-   `Basis<class_Basis>` **get\_inertia\_tensor**()

**Deprecated:** This property may be changed or removed in future
versions.

The inertia tensor of the physics body, in kilogram meter squared
(kg⋅m²). This is only used when the body type is "rigid" or "vehicle".

When converted to a Godot `RigidBody3D<class_RigidBody3D>` node, if this
value is zero, then the inertia will be calculated automatically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **linear\_velocity** = `Vector3(0, 0, 0)`
`🔗<class_GLTFPhysicsBody_property_linear_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_linear\_velocity**()

The linear velocity of the physics body, in meters per second. This is
only used when the body type is "rigid" or "vehicle".

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **mass** = `1.0`
`🔗<class_GLTFPhysicsBody_property_mass>`

classref-property-setget

-   `void (No return value.)` **set\_mass**(value: `float<class_float>`)
-   `float<class_float>` **get\_mass**()

The mass of the physics body, in kilograms. This is only used when the
body type is "rigid" or "vehicle".

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`GLTFPhysicsBody<class_GLTFPhysicsBody>`
**from\_dictionary**(dictionary: `Dictionary<class_Dictionary>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFPhysicsBody_method_from_dictionary>`

Creates a new GLTFPhysicsBody instance by parsing the given
`Dictionary<class_Dictionary>` in the `OMI_physics_body` glTF extension
format.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GLTFPhysicsBody<class_GLTFPhysicsBody>` **from\_node**(body\_node:
`CollisionObject3D<class_CollisionObject3D>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFPhysicsBody_method_from_node>`

Creates a new GLTFPhysicsBody instance from the given Godot
`CollisionObject3D<class_CollisionObject3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **to\_dictionary**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GLTFPhysicsBody_method_to_dictionary>`

Serializes this GLTFPhysicsBody instance into a
`Dictionary<class_Dictionary>`. It will be in the format expected by the
`OMI_physics_body` glTF extension.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CollisionObject3D<class_CollisionObject3D>` **to\_node**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GLTFPhysicsBody_method_to_node>`

Converts this GLTFPhysicsBody instance into a Godot
`CollisionObject3D<class_CollisionObject3D>` node.
