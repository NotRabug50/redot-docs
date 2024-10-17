github\_url  
hide

# MeshInstance2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Node used for displaying a `Mesh<class_Mesh>` in 2D.

classref-introduction-group

## Description

Node used for displaying a `Mesh<class_Mesh>` in 2D. A
**MeshInstance2D** can be automatically created from an existing
`Sprite2D<class_Sprite2D>` via a tool in the editor toolbar. Select the
`Sprite2D<class_Sprite2D>` node, then choose **Sprite2D &gt; Convert to
MeshInstance2D** at the top of the 2D editor viewport.

classref-introduction-group

## Tutorials

-   `2D meshes <../tutorials/2d/2d_meshes>`

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**texture\_changed**() `🔗<class_MeshInstance2D_signal_texture_changed>`

Emitted when the `texture<class_MeshInstance2D_property_texture>` is
changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Mesh<class_Mesh>` **mesh** `🔗<class_MeshInstance2D_property_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_mesh**(value: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_mesh**()

The `Mesh<class_Mesh>` that will be drawn by the **MeshInstance2D**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_MeshInstance2D_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

The `Texture2D<class_Texture2D>` that will be used if using the default
`CanvasItemMaterial<class_CanvasItemMaterial>`. Can be accessed as
`TEXTURE` in CanvasItem shader.
