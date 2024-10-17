github\_url  
hide

# PlaceholderMaterial

**Inherits:** `Material<class_Material>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Placeholder class for a material.

classref-introduction-group

## Description

This class is used when loading a project that uses a
`Material<class_Material>` subclass in 2 conditions:

-   When running the project exported in dedicated server mode, only the
    texture's dimensions are kept (as they may be relied upon for
    gameplay purposes or positioning of other elements). This allows
    reducing the exported PCK's size significantly.
-   When this subclass is missing due to using a different engine
    version or build (e.g. modules disabled).
