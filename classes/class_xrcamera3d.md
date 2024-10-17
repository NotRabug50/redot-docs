github\_url  
hide

# XRCamera3D

**Inherits:** `Camera3D<class_Camera3D>` **&lt;** `Node3D<class_Node3D>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A camera node with a few overrules for AR/VR applied, such as location
tracking.

classref-introduction-group

## Description

This is a helper spatial node for our camera; note that, if stereoscopic
rendering is applicable (VR-HMD), most of the camera properties are
ignored, as the HMD information overrides them. The only properties that
can be trusted are the near and far planes.

The position and orientation of this node is automatically updated by
the XR Server to represent the location of the HMD if such tracking is
available and can thus be used by game logic. Note that, in contrast to
the XR Controller, the render thread has access to the most up-to-date
tracking data of the HMD and the location of the XRCamera3D can lag a
few milliseconds behind what is used for rendering as a result.

classref-introduction-group

## Tutorials

-   `XR documentation index <../tutorials/xr/index>`
