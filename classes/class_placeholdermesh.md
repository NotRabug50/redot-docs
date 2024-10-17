github\_url  
hide

# PlaceholderMesh

**Inherits:** `Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Placeholder class for a mesh.

classref-introduction-group

## Description

This class is used when loading a project that uses a `Mesh<class_Mesh>`
subclass in 2 conditions:

-   When running the project exported in dedicated server mode, only the
    texture's dimensions are kept (as they may be relied upon for
    gameplay purposes or positioning of other elements). This allows
    reducing the exported PCK's size significantly.
-   When this subclass is missing due to using a different engine
    version or build (e.g. modules disabled).

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

`AABB<class_AABB>` **aabb** = `AABB(0, 0, 0, 0, 0, 0)`
`🔗<class_PlaceholderMesh_property_aabb>`

classref-property-setget

-   `void (No return value.)` **set\_aabb**(value: `AABB<class_AABB>`)
-   `AABB<class_AABB>` **get\_aabb**()

The smallest `AABB<class_AABB>` enclosing this mesh in local space.
