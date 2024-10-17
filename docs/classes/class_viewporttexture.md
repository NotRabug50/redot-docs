github\_url  
hide

# ViewportTexture

**Inherits:** `Texture2D<class_Texture2D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Provides the content of a `Viewport<class_Viewport>` as a dynamic
texture.

classref-introduction-group

## Description

A **ViewportTexture** provides the content of a
`Viewport<class_Viewport>` as a dynamic `Texture2D<class_Texture2D>`.
This can be used to combine the rendering of `Control<class_Control>`,
`Node2D<class_Node2D>` and `Node3D<class_Node3D>` nodes. For example,
you can use this texture to display a 3D scene inside a
`TextureRect<class_TextureRect>`, or a 2D overlay in a
`Sprite3D<class_Sprite3D>`.

To get a **ViewportTexture** in code, use the
`Viewport.get_texture<class_Viewport_method_get_texture>` method on the
target viewport.

\*\*Note:\*\* A **ViewportTexture** is always local to its scene (see
`Resource.resource_local_to_scene<class_Resource_property_resource_local_to_scene>`).
If the scene root is not ready, it may return incorrect data (see
`Node.ready<class_Node_signal_ready>`).

\*\*Note:\*\* Instantiating scenes containing a high-resolution
**ViewportTexture** may cause noticeable stutter.

\*\*Note:\*\* When using a `Viewport<class_Viewport>` with
`Viewport.use_hdr_2d<class_Viewport_property_use_hdr_2d>` set to `true`
the returned texture will be an HDR image encoded in linear space. This
may look darker than normal when displayed directly on screen. To
convert to gamma space, you can do the following:

    img.convert(Image.FORMAT_RGBA8)
    imb.linear_to_srgb()

classref-introduction-group

## Tutorials

-   [GUI in 3D Viewport
    Demo](https://godotengine.org/asset-library/asset/2807)
-   [3D in 2D Viewport
    Demo](https://godotengine.org/asset-library/asset/2804)
-   [2D in 3D Viewport
    Demo](https://godotengine.org/asset-library/asset/2803)
-   [3D Resolution Scaling
    Demo](https://godotengine.org/asset-library/asset/2805)

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

`NodePath<class_NodePath>` **viewport\_path** = `NodePath("")`
`🔗<class_ViewportTexture_property_viewport_path>`

classref-property-setget

-   `void (No return value.)` **set\_viewport\_path\_in\_scene**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_viewport\_path\_in\_scene**()

The path to the `Viewport<class_Viewport>` node to display. This is
relative to the local scene root (see
`Resource.get_local_scene<class_Resource_method_get_local_scene>`),
**not** to the nodes that use this texture.

\*\*Note:\*\* In the editor, this path is automatically updated when the
target viewport or one of its ancestors is renamed or moved. At runtime,
this path may not automatically update if the scene root cannot be
found.
