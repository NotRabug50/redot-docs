github\_url  
hide

# StyleBoxFlat

**Inherits:** `StyleBox<class_StyleBox>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A customizable `StyleBox<class_StyleBox>` that doesn't use a texture.

classref-introduction-group

## Description

By configuring various properties of this style box, you can achieve
many common looks without the need of a texture. This includes
optionally rounded borders, antialiasing, shadows, and skew.

Setting corner radius to high values is allowed. As soon as corners
overlap, the stylebox will switch to a relative system:

    height = 30
    corner_radius_top_left = 50
    corner_radius_bottom_left = 100

The relative system now would take the 1:2 ratio of the two left corners
to calculate the actual corner width. Both corners added will **never**
be more than the height. Result:

    corner_radius_top_left: 10
    corner_radius_bottom_left: 20

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

`bool<class_bool>` **anti\_aliasing** = `true`
`🔗<class_StyleBoxFlat_property_anti_aliasing>`

classref-property-setget

-   `void (No return value.)` **set\_anti\_aliased**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_anti\_aliased**()

Antialiasing draws a small ring around the edges, which fades to
transparency. As a result, edges look much smoother. This is only
noticeable when using rounded corners or
`skew<class_StyleBoxFlat_property_skew>`.

\*\*Note:\*\* When using beveled corners with 45-degree angles
(`corner_detail<class_StyleBoxFlat_property_corner_detail>` = 1), it is
recommended to set
`anti_aliasing<class_StyleBoxFlat_property_anti_aliasing>` to `false` to
ensure crisp visuals and avoid possible visual glitches.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anti\_aliasing\_size** = `1.0`
`🔗<class_StyleBoxFlat_property_anti_aliasing_size>`

classref-property-setget

-   `void (No return value.)` **set\_aa\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_aa\_size**()

This changes the size of the antialiasing effect. `1.0` is recommended
for an optimal result at 100% scale, identical to how rounded rectangles
are rendered in web browsers and most vector drawing software.

\*\*Note:\*\* Higher values may produce a blur effect but can also
create undesired artifacts on small boxes with large-radius corners.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **bg\_color** = `Color(0.6, 0.6, 0.6, 1)`
`🔗<class_StyleBoxFlat_property_bg_color>`

classref-property-setget

-   `void (No return value.)` **set\_bg\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_bg\_color**()

The background color of the stylebox.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **border\_blend** = `false`
`🔗<class_StyleBoxFlat_property_border_blend>`

classref-property-setget

-   `void (No return value.)` **set\_border\_blend**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_border\_blend**()

If `true`, the border will fade into the background color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **border\_color** = `Color(0.8, 0.8, 0.8, 1)`
`🔗<class_StyleBoxFlat_property_border_color>`

classref-property-setget

-   `void (No return value.)` **set\_border\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_border\_color**()

Sets the color of the border.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **border\_width\_bottom** = `0`
`🔗<class_StyleBoxFlat_property_border_width_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_border\_width**(margin:
    `Side<enum_@GlobalScope_Side>`, width: `int<class_int>`)
-   `int<class_int>` **get\_border\_width**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Border width for the bottom border.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **border\_width\_left** = `0`
`🔗<class_StyleBoxFlat_property_border_width_left>`

classref-property-setget

-   `void (No return value.)` **set\_border\_width**(margin:
    `Side<enum_@GlobalScope_Side>`, width: `int<class_int>`)
-   `int<class_int>` **get\_border\_width**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Border width for the left border.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **border\_width\_right** = `0`
`🔗<class_StyleBoxFlat_property_border_width_right>`

classref-property-setget

-   `void (No return value.)` **set\_border\_width**(margin:
    `Side<enum_@GlobalScope_Side>`, width: `int<class_int>`)
-   `int<class_int>` **get\_border\_width**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Border width for the right border.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **border\_width\_top** = `0`
`🔗<class_StyleBoxFlat_property_border_width_top>`

classref-property-setget

-   `void (No return value.)` **set\_border\_width**(margin:
    `Side<enum_@GlobalScope_Side>`, width: `int<class_int>`)
-   `int<class_int>` **get\_border\_width**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Border width for the top border.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **corner\_detail** = `8`
`🔗<class_StyleBoxFlat_property_corner_detail>`

classref-property-setget

-   `void (No return value.)` **set\_corner\_detail**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_corner\_detail**()

This sets the number of vertices used for each corner. Higher values
result in rounder corners but take more processing power to compute.
When choosing a value, you should take the corner radius
(`set_corner_radius_all<class_StyleBoxFlat_method_set_corner_radius_all>`)
into account.

For corner radii less than 10, `4` or `5` should be enough. For corner
radii less than 30, values between `8` and `12` should be enough.

A corner detail of `1` will result in chamfered corners instead of
rounded corners, which is useful for some artistic effects.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **corner\_radius\_bottom\_left** = `0`
`🔗<class_StyleBoxFlat_property_corner_radius_bottom_left>`

classref-property-setget

-   `void (No return value.)` **set\_corner\_radius**(corner:
    `Corner<enum_@GlobalScope_Corner>`, radius: `int<class_int>`)
-   `int<class_int>` **get\_corner\_radius**(corner:
    `Corner<enum_@GlobalScope_Corner>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The bottom-left corner's radius. If `0`, the corner is not rounded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **corner\_radius\_bottom\_right** = `0`
`🔗<class_StyleBoxFlat_property_corner_radius_bottom_right>`

classref-property-setget

-   `void (No return value.)` **set\_corner\_radius**(corner:
    `Corner<enum_@GlobalScope_Corner>`, radius: `int<class_int>`)
-   `int<class_int>` **get\_corner\_radius**(corner:
    `Corner<enum_@GlobalScope_Corner>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The bottom-right corner's radius. If `0`, the corner is not rounded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **corner\_radius\_top\_left** = `0`
`🔗<class_StyleBoxFlat_property_corner_radius_top_left>`

classref-property-setget

-   `void (No return value.)` **set\_corner\_radius**(corner:
    `Corner<enum_@GlobalScope_Corner>`, radius: `int<class_int>`)
-   `int<class_int>` **get\_corner\_radius**(corner:
    `Corner<enum_@GlobalScope_Corner>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The top-left corner's radius. If `0`, the corner is not rounded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **corner\_radius\_top\_right** = `0`
`🔗<class_StyleBoxFlat_property_corner_radius_top_right>`

classref-property-setget

-   `void (No return value.)` **set\_corner\_radius**(corner:
    `Corner<enum_@GlobalScope_Corner>`, radius: `int<class_int>`)
-   `int<class_int>` **get\_corner\_radius**(corner:
    `Corner<enum_@GlobalScope_Corner>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The top-right corner's radius. If `0`, the corner is not rounded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **draw\_center** = `true`
`🔗<class_StyleBoxFlat_property_draw_center>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_center**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_draw\_center\_enabled**()

Toggles drawing of the inner part of the stylebox.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **expand\_margin\_bottom** = `0.0`
`🔗<class_StyleBoxFlat_property_expand_margin_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Expands the stylebox outside of the control rect on the bottom edge.
Useful in combination with
`border_width_bottom<class_StyleBoxFlat_property_border_width_bottom>`
to draw a border outside the control rect.

\*\*Note:\*\* Unlike
`StyleBox.content_margin_bottom<class_StyleBox_property_content_margin_bottom>`,
`expand_margin_bottom<class_StyleBoxFlat_property_expand_margin_bottom>`
does *not* affect the size of the clickable area for
`Control<class_Control>`s. This can negatively impact usability if used
wrong, as the user may try to click an area of the StyleBox that cannot
actually receive clicks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **expand\_margin\_left** = `0.0`
`🔗<class_StyleBoxFlat_property_expand_margin_left>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Expands the stylebox outside of the control rect on the left edge.
Useful in combination with
`border_width_left<class_StyleBoxFlat_property_border_width_left>` to
draw a border outside the control rect.

\*\*Note:\*\* Unlike
`StyleBox.content_margin_left<class_StyleBox_property_content_margin_left>`,
`expand_margin_left<class_StyleBoxFlat_property_expand_margin_left>`
does *not* affect the size of the clickable area for
`Control<class_Control>`s. This can negatively impact usability if used
wrong, as the user may try to click an area of the StyleBox that cannot
actually receive clicks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **expand\_margin\_right** = `0.0`
`🔗<class_StyleBoxFlat_property_expand_margin_right>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Expands the stylebox outside of the control rect on the right edge.
Useful in combination with
`border_width_right<class_StyleBoxFlat_property_border_width_right>` to
draw a border outside the control rect.

\*\*Note:\*\* Unlike
`StyleBox.content_margin_right<class_StyleBox_property_content_margin_right>`,
`expand_margin_right<class_StyleBoxFlat_property_expand_margin_right>`
does *not* affect the size of the clickable area for
`Control<class_Control>`s. This can negatively impact usability if used
wrong, as the user may try to click an area of the StyleBox that cannot
actually receive clicks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **expand\_margin\_top** = `0.0`
`🔗<class_StyleBoxFlat_property_expand_margin_top>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Expands the stylebox outside of the control rect on the top edge. Useful
in combination with
`border_width_top<class_StyleBoxFlat_property_border_width_top>` to draw
a border outside the control rect.

\*\*Note:\*\* Unlike
`StyleBox.content_margin_top<class_StyleBox_property_content_margin_top>`,
`expand_margin_top<class_StyleBoxFlat_property_expand_margin_top>` does
*not* affect the size of the clickable area for
`Control<class_Control>`s. This can negatively impact usability if used
wrong, as the user may try to click an area of the StyleBox that cannot
actually receive clicks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **shadow\_color** = `Color(0, 0, 0, 0.6)`
`🔗<class_StyleBoxFlat_property_shadow_color>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_shadow\_color**()

The color of the shadow. This has no effect if
`shadow_size<class_StyleBoxFlat_property_shadow_size>` is lower than 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **shadow\_offset** = `Vector2(0, 0)`
`🔗<class_StyleBoxFlat_property_shadow_offset>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_shadow\_offset**()

The shadow offset in pixels. Adjusts the position of the shadow
relatively to the stylebox.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **shadow\_size** = `0`
`🔗<class_StyleBoxFlat_property_shadow_size>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_shadow\_size**()

The shadow size in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **skew** = `Vector2(0, 0)`
`🔗<class_StyleBoxFlat_property_skew>`

classref-property-setget

-   `void (No return value.)` **set\_skew**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_skew**()

If set to a non-zero value on either axis,
`skew<class_StyleBoxFlat_property_skew>` distorts the StyleBox
horizontally and/or vertically. This can be used for "futuristic"-style
UIs. Positive values skew the StyleBox towards the right (X axis) and
upwards (Y axis), while negative values skew the StyleBox towards the
left (X axis) and downwards (Y axis).

\*\*Note:\*\* To ensure text does not touch the StyleBox's edges,
consider increasing the `StyleBox<class_StyleBox>`'s content margin (see
`StyleBox.content_margin_bottom<class_StyleBox_property_content_margin_bottom>`).
It is preferable to increase the content margin instead of the expand
margin (see
`expand_margin_bottom<class_StyleBoxFlat_property_expand_margin_bottom>`),
as increasing the expand margin does not increase the size of the
clickable area for `Control<class_Control>`s.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_border\_width**(margin:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBoxFlat_method_get_border_width>`

Returns the specified `Side<enum_@GlobalScope_Side>`'s border width.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_border\_width\_min**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBoxFlat_method_get_border_width_min>`

Returns the smallest border width out of all four borders.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_corner\_radius**(corner:
`Corner<enum_@GlobalScope_Corner>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBoxFlat_method_get_corner_radius>`

Returns the given `corner`'s radius. See
`Corner<enum_@GlobalScope_Corner>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_expand\_margin**(margin:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBoxFlat_method_get_expand_margin>`

Returns the size of the specified `Side<enum_@GlobalScope_Side>`'s
expand margin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_border\_width**(margin:
`Side<enum_@GlobalScope_Side>`, width: `int<class_int>`)
`🔗<class_StyleBoxFlat_method_set_border_width>`

Sets the specified `Side<enum_@GlobalScope_Side>`'s border width to
`width` pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_border\_width\_all**(width:
`int<class_int>`) `🔗<class_StyleBoxFlat_method_set_border_width_all>`

Sets the border width to `width` pixels for all sides.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_corner\_radius**(corner:
`Corner<enum_@GlobalScope_Corner>`, radius: `int<class_int>`)
`🔗<class_StyleBoxFlat_method_set_corner_radius>`

Sets the corner radius to `radius` pixels for the given `corner`. See
`Corner<enum_@GlobalScope_Corner>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_corner\_radius\_all**(radius:
`int<class_int>`) `🔗<class_StyleBoxFlat_method_set_corner_radius_all>`

Sets the corner radius to `radius` pixels for all corners.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_expand\_margin**(margin:
`Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
`🔗<class_StyleBoxFlat_method_set_expand_margin>`

Sets the expand margin to `size` pixels for the specified
`Side<enum_@GlobalScope_Side>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_expand\_margin\_all**(size:
`float<class_float>`)
`🔗<class_StyleBoxFlat_method_set_expand_margin_all>`

Sets the expand margin to `size` pixels for all sides.
