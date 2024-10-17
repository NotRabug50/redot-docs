github\_url  
hide

# HeightMapShape3D

**Inherits:** `Shape3D<class_Shape3D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 3D height map shape used for physics collision.

classref-introduction-group

## Description

A 3D heightmap shape, intended for use in physics. Usually used to
provide a shape for a `CollisionShape3D<class_CollisionShape3D>`. This
is useful for terrain, but it is limited as overhangs (such as caves)
cannot be stored. Holes in a **HeightMapShape3D** are created by
assigning very low values to points in the desired area.

\*\*Performance:\*\* **HeightMapShape3D** is faster to check collisions
against than `ConcavePolygonShape3D<class_ConcavePolygonShape3D>`, but
it is significantly slower than primitive shapes like
`BoxShape3D<class_BoxShape3D>`.

A heightmap collision shape can also be build by using an
`Image<class_Image>` reference:

gdscript

var heightmap\_texture: Texture =
ResourceLoader.load("<res://heightmap_image.exr>") var heightmap\_image:
Image = heightmap\_texture.get\_image()
heightmap\_image.convert(Image.FORMAT\_RF)

var height\_min: float = 0.0 var height\_max: float = 10.0

update\_map\_data\_from\_image(heightmap\_image, height\_min,
height\_max)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PackedFloat32Array<class_PackedFloat32Array>` **map\_data** =
`PackedFloat32Array(0, 0, 0, 0)`
`🔗<class_HeightMapShape3D_property_map_data>`

classref-property-setget

-   `void (No return value.)` **set\_map\_data**(value:
    `PackedFloat32Array<class_PackedFloat32Array>`)
-   `PackedFloat32Array<class_PackedFloat32Array>` **get\_map\_data**()

Height map data. The array's size must be equal to
`map_width<class_HeightMapShape3D_property_map_width>` multiplied by
`map_depth<class_HeightMapShape3D_property_map_depth>`.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedFloat32Array<class_PackedFloat32Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **map\_depth** = `2`
`🔗<class_HeightMapShape3D_property_map_depth>`

classref-property-setget

-   `void (No return value.)` **set\_map\_depth**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_map\_depth**()

Number of vertices in the depth of the height map. Changing this will
resize the `map_data<class_HeightMapShape3D_property_map_data>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **map\_width** = `2`
`🔗<class_HeightMapShape3D_property_map_width>`

classref-property-setget

-   `void (No return value.)` **set\_map\_width**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_map\_width**()

Number of vertices in the width of the height map. Changing this will
resize the `map_data<class_HeightMapShape3D_property_map_data>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_max\_height**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_HeightMapShape3D_method_get_max_height>`

Returns the largest height value found in
`map_data<class_HeightMapShape3D_property_map_data>`. Recalculates only
when `map_data<class_HeightMapShape3D_property_map_data>` changes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_min\_height**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_HeightMapShape3D_method_get_min_height>`

Returns the smallest height value found in
`map_data<class_HeightMapShape3D_property_map_data>`. Recalculates only
when `map_data<class_HeightMapShape3D_property_map_data>` changes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_map\_data\_from\_image**(image:
`Image<class_Image>`, height\_min: `float<class_float>`, height\_max:
`float<class_float>`)
`🔗<class_HeightMapShape3D_method_update_map_data_from_image>`

Updates `map_data<class_HeightMapShape3D_property_map_data>` with data
read from an `Image<class_Image>` reference. Automatically resizes
heightmap `map_width<class_HeightMapShape3D_property_map_width>` and
`map_depth<class_HeightMapShape3D_property_map_depth>` to fit the full
image width and height.

The image needs to be in either
`Image.FORMAT_RF<class_Image_constant_FORMAT_RF>` (32 bit),
`Image.FORMAT_RH<class_Image_constant_FORMAT_RH>` (16 bit), or
`Image.FORMAT_R8<class_Image_constant_FORMAT_R8>` (8 bit).

Each image pixel is read in as a float on the range from `0.0` (black
pixel) to `1.0` (white pixel). This range value gets remapped to
`height_min` and `height_max` to form the final height value.
