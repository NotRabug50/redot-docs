github\_url  
hide

# FBXState

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `GLTFState<class_GLTFState>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

classref-introduction-group

## Description

The FBXState handles the state data imported from FBX files.

classref-reftable-group

## Properties

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

`bool<class_bool>` **allow\_geometry\_helper\_nodes** = `false`
`🔗<class_FBXState_property_allow_geometry_helper_nodes>`

classref-property-setget

-   `void (No return value.)`
    **set\_allow\_geometry\_helper\_nodes**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_allow\_geometry\_helper\_nodes**()

If `true`, the import process used auxiliary nodes called geometry
helper nodes. These nodes help preserve the pivots and transformations
of the original 3D model during import.
