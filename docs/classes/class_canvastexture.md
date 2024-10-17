github\_url  
hide

# CanvasTexture

**Inherits:** `Texture2D<class_Texture2D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Texture with optional normal and specular maps for use in 2D rendering.

classref-introduction-group

## Description

**CanvasTexture** is an alternative to
`ImageTexture<class_ImageTexture>` for 2D rendering. It allows using
normal maps and specular maps in any node that inherits from
`CanvasItem<class_CanvasItem>`. **CanvasTexture** also allows overriding
the texture's filter and repeat mode independently of the node's
properties (or the project settings).

\*\*Note:\*\* **CanvasTexture** cannot be used in 3D. It will not
display correctly when applied to any
`VisualInstance3D<class_VisualInstance3D>`, such as
`Sprite3D<class_Sprite3D>` or `Decal<class_Decal>`. For physically-based
materials in 3D, use `BaseMaterial3D<class_BaseMaterial3D>` instead.

classref-introduction-group

## Tutorials

-   `2D Lights and Shadows <../tutorials/2d/2d_lights_and_shadows>`

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

## Property Descriptions

classref-property

`Texture2D<class_Texture2D>` **diffuse\_texture**
`🔗<class_CanvasTexture_property_diffuse_texture>`

classref-property-setget

-   `void (No return value.)` **set\_diffuse\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_diffuse\_texture**()

The diffuse (color) texture to use. This is the main texture you want to
set in most cases.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **normal\_texture**
`🔗<class_CanvasTexture_property_normal_texture>`

classref-property-setget

-   `void (No return value.)` **set\_normal\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_normal\_texture**()

The normal map texture to use. Only has a visible effect if
`Light2D<class_Light2D>`s are affecting this **CanvasTexture**.

\*\*Note:\*\* Godot expects the normal map to use X+, Y+, and Z+
coordinates. See [this
page](http://wiki.polycount.com/wiki/Normal_Map_Technical_Details#Common_Swizzle_Coordinates)
for a comparison of normal map coordinates expected by popular engines.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **specular\_color** = `Color(1, 1, 1, 1)`
`🔗<class_CanvasTexture_property_specular_color>`

classref-property-setget

-   `void (No return value.)` **set\_specular\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_specular\_color**()

The multiplier for specular reflection colors. The
`Light2D<class_Light2D>`'s color is also taken into account when
determining the reflection color. Only has a visible effect if
`Light2D<class_Light2D>`s are affecting this **CanvasTexture**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **specular\_shininess** = `1.0`
`🔗<class_CanvasTexture_property_specular_shininess>`

classref-property-setget

-   `void (No return value.)` **set\_specular\_shininess**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_specular\_shininess**()

The specular exponent for `Light2D<class_Light2D>` specular reflections.
Higher values result in a more glossy/"wet" look, with reflections
becoming more localized and less visible overall. The default value of
`1.0` disables specular reflections entirely. Only has a visible effect
if `Light2D<class_Light2D>`s are affecting this **CanvasTexture**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **specular\_texture**
`🔗<class_CanvasTexture_property_specular_texture>`

classref-property-setget

-   `void (No return value.)` **set\_specular\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_specular\_texture**()

The specular map to use for `Light2D<class_Light2D>` specular
reflections. This should be a grayscale or colored texture, with
brighter areas resulting in a higher
`specular_shininess<class_CanvasTexture_property_specular_shininess>`
value. Using a colored
`specular_texture<class_CanvasTexture_property_specular_texture>` allows
controlling specular shininess on a per-channel basis. Only has a
visible effect if `Light2D<class_Light2D>`s are affecting this
**CanvasTexture**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureFilter<enum_CanvasItem_TextureFilter>` **texture\_filter** = `0`
`🔗<class_CanvasTexture_property_texture_filter>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_filter**(value:
    `TextureFilter<enum_CanvasItem_TextureFilter>`)
-   `TextureFilter<enum_CanvasItem_TextureFilter>`
    **get\_texture\_filter**()

The texture filtering mode to use when drawing this **CanvasTexture**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureRepeat<enum_CanvasItem_TextureRepeat>` **texture\_repeat** = `0`
`🔗<class_CanvasTexture_property_texture_repeat>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_repeat**(value:
    `TextureRepeat<enum_CanvasItem_TextureRepeat>`)
-   `TextureRepeat<enum_CanvasItem_TextureRepeat>`
    **get\_texture\_repeat**()

The texture repeat mode to use when drawing this **CanvasTexture**.
