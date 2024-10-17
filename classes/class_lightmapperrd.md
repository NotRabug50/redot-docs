github\_url  
hide

# LightmapperRD

**Inherits:** `Lightmapper<class_Lightmapper>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

The built-in GPU-based lightmapper for use with
`LightmapGI<class_LightmapGI>`.

classref-introduction-group

## Description

LightmapperRD ("RD" stands for `RenderingDevice<class_RenderingDevice>`)
is the built-in GPU-based lightmapper for use with
`LightmapGI<class_LightmapGI>`. On most dedicated GPUs, it can bake
lightmaps much faster than most CPU-based lightmappers. LightmapperRD
uses compute shaders to bake lightmaps, so it does not require CUDA or
OpenCL libraries to be installed to be usable.

\*\*Note:\*\* Only usable when using the Vulkan backend (Forward+ or
Mobile), not OpenGL.
