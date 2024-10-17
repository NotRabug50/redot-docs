github\_url  
hide

# CanvasGroup

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Merges several 2D nodes into a single draw operation.

classref-introduction-group

## Description

Child `CanvasItem<class_CanvasItem>` nodes of a **CanvasGroup** are
drawn as a single object. It allows to e.g. draw overlapping translucent
2D nodes without blending (set
`CanvasItem.self_modulate<class_CanvasItem_property_self_modulate>`
property of **CanvasGroup** to achieve this effect).

\*\*Note:\*\* The **CanvasGroup** uses a custom shader to read from the
backbuffer to draw its children. Assigning a `Material<class_Material>`
to the **CanvasGroup** overrides the builtin shader. To duplicate the
behavior of the builtin shader in a custom `Shader<class_Shader>` use
the following:

    shader_type canvas_item;
    render_mode unshaded;

    uniform sampler2D screen_texture : hint_screen_texture, repeat_disable, filter_nearest;

    void fragment() {
        vec4 c = textureLod(screen_texture, SCREEN_UV, 0.0);

        if (c.a > 0.0001) {
            c.rgb /= c.a;
        }

        COLOR *= c;
    }

\*\*Note:\*\* Since **CanvasGroup** and
`CanvasItem.clip_children<class_CanvasItem_property_clip_children>` both
utilize the backbuffer, children of a **CanvasGroup** who have their
`CanvasItem.clip_children<class_CanvasItem_property_clip_children>` set
to anything other than
`CanvasItem.CLIP_CHILDREN_DISABLED<class_CanvasItem_constant_CLIP_CHILDREN_DISABLED>`
will not function correctly.

classref-reftable-group

## Properties

<table>
<tbody>
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

## Property Descriptions

classref-property

`float<class_float>` **clear\_margin** = `10.0`
`🔗<class_CanvasGroup_property_clear_margin>`

classref-property-setget

-   `void (No return value.)` **set\_clear\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_clear\_margin**()

Sets the size of the margin used to expand the clearing rect of this
**CanvasGroup**. This expands the area of the backbuffer that will be
used by the **CanvasGroup**. A smaller margin will reduce the area of
the backbuffer used which can increase performance, however if
`use_mipmaps<class_CanvasGroup_property_use_mipmaps>` is enabled, a
small margin may result in mipmap errors at the edge of the
**CanvasGroup**. Accordingly, this should be left as small as possible,
but should be increased if artifacts appear along the edges of the
canvas group.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fit\_margin** = `10.0`
`🔗<class_CanvasGroup_property_fit_margin>`

classref-property-setget

-   `void (No return value.)` **set\_fit\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fit\_margin**()

Sets the size of a margin used to expand the drawable rect of this
**CanvasGroup**. The size of the **CanvasGroup** is determined by
fitting a rect around its children then expanding that rect by
`fit_margin<class_CanvasGroup_property_fit_margin>`. This increases both
the backbuffer area used and the area covered by the **CanvasGroup**
both of which can reduce performance. This should be kept as small as
possible and should only be expanded when an increased size is needed
(e.g. for custom shader effects).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_mipmaps** = `false`
`🔗<class_CanvasGroup_property_use_mipmaps>`

classref-property-setget

-   `void (No return value.)` **set\_use\_mipmaps**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_mipmaps**()

If `true`, calculates mipmaps for the backbuffer before drawing the
**CanvasGroup** so that mipmaps can be used in a custom
`ShaderMaterial<class_ShaderMaterial>` attached to the **CanvasGroup**.
Generating mipmaps has a performance cost so this should not be enabled
unless required.
