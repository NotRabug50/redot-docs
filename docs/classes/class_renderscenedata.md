github\_url  
hide

# RenderSceneData

**Inherits:** `Object<class_Object>`

**Inherited By:**
`RenderSceneDataExtension<class_RenderSceneDataExtension>`,
`RenderSceneDataRD<class_RenderSceneDataRD>`

Abstract render data object, holds scene data related to rendering a
single frame of a viewport.

classref-introduction-group

## Description

Abstract scene data object, exists for the duration of rendering a
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

`Projection<class_Projection>` **get\_cam\_projection**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderSceneData_method_get_cam_projection>`

Returns the camera projection used to render this frame.

\*\*Note:\*\* If more than one view is rendered, this will return a
combined projection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_cam\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderSceneData_method_get_cam_transform>`

Returns the camera transform used to render this frame.

\*\*Note:\*\* If more than one view is rendered, this will return a
centered transform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_uniform\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderSceneData_method_get_uniform_buffer>`

Return the `RID<class_RID>` of the uniform buffer containing the scene
data as a UBO.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_view\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderSceneData_method_get_view_count>`

Returns the number of views being rendered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_view\_eye\_offset**(view:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderSceneData_method_get_view_eye_offset>`

Returns the eye offset per view used to render this frame. This is the
offset between our camera transform and the eye transform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Projection<class_Projection>` **get\_view\_projection**(view:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RenderSceneData_method_get_view_projection>`

Returns the view projection per view used to render this frame.

\*\*Note:\*\* If a single view is rendered, this returns the camera
projection. If more than one view is rendered, this will return a
projection for the given view including the eye offset.
