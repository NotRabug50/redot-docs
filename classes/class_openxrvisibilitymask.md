github\_url  
hide

# OpenXRVisibilityMask

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Draws a stereo correct visibility mask.

classref-introduction-group

## Description

The visibility mask allows us to black out the part of the render result
that is invisible due to lens distortion.

As this is rendered first, it prevents fragments with expensive lighting
calculations to be processed as they are discarded through z-checking.
