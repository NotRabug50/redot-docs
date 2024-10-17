github\_url  
hide

# RenderData

**Inherits:** `Object<class_Object>`

**Inherited By:** `RenderDataExtension<class_RenderDataExtension>`,
`RenderDataRD<class_RenderDataRD>`

Abstract render data object, holds frame data related to rendering a
single frame of a viewport.

classref-introduction-group

## Description

Abstract render data object, exists for the duration of rendering a
single viewport.

\*\*Note:\*\* This is an internal rendering server object, do not
instantiate this from script.

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

## Method Descriptions

classref-method

`RID<class_RID>` **get\_camera\_attributes**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderData_method_get_camera_attributes>`

Returns the `RID<class_RID>` of the camera attributes object in the
`RenderingServer<class_RenderingServer>` being used to render this
viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_environment**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderData_method_get_environment>`

Returns the `RID<class_RID>` of the environments object in the
`RenderingServer<class_RenderingServer>` being used to render this
viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RenderSceneBuffers<class_RenderSceneBuffers>`
**get\_render\_scene\_buffers**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderData_method_get_render_scene_buffers>`

Returns the `RenderSceneBuffers<class_RenderSceneBuffers>` object
managing the scene buffers for rendering this viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RenderSceneData<class_RenderSceneData>` **get\_render\_scene\_data**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderData_method_get_render_scene_data>`

Returns the `RenderSceneData<class_RenderSceneData>` object managing
this frames scene data.
