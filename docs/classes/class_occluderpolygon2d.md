github\_url  
hide

# OccluderPolygon2D

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Defines a 2D polygon for LightOccluder2D.

classref-introduction-group

## Description

Editor facility that helps you draw a 2D polygon used as resource for
`LightOccluder2D<class_LightOccluder2D>`.

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

## Enumerations

classref-enumeration

enum **CullMode**: `🔗<enum_OccluderPolygon2D_CullMode>`

classref-enumeration-constant

`CullMode<enum_OccluderPolygon2D_CullMode>` **CULL\_DISABLED** = `0`

Culling is disabled. See
`cull_mode<class_OccluderPolygon2D_property_cull_mode>`.

classref-enumeration-constant

`CullMode<enum_OccluderPolygon2D_CullMode>` **CULL\_CLOCKWISE** = `1`

Culling is performed in the clockwise direction. See
`cull_mode<class_OccluderPolygon2D_property_cull_mode>`.

classref-enumeration-constant

`CullMode<enum_OccluderPolygon2D_CullMode>` **CULL\_COUNTER\_CLOCKWISE**
= `2`

Culling is performed in the counterclockwise direction. See
`cull_mode<class_OccluderPolygon2D_property_cull_mode>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **closed** = `true`
`🔗<class_OccluderPolygon2D_property_closed>`

classref-property-setget

-   `void (No return value.)` **set\_closed**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_closed**()

If `true`, closes the polygon. A closed OccluderPolygon2D occludes the
light coming from any direction. An opened OccluderPolygon2D occludes
the light only at its outline's direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CullMode<enum_OccluderPolygon2D_CullMode>` **cull\_mode** = `0`
`🔗<class_OccluderPolygon2D_property_cull_mode>`

classref-property-setget

-   `void (No return value.)` **set\_cull\_mode**(value:
    `CullMode<enum_OccluderPolygon2D_CullMode>`)
-   `CullMode<enum_OccluderPolygon2D_CullMode>` **get\_cull\_mode**()

The culling mode to use.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedVector2Array<class_PackedVector2Array>` **polygon** =
`PackedVector2Array()` `🔗<class_OccluderPolygon2D_property_polygon>`

classref-property-setget

-   `void (No return value.)` **set\_polygon**(value:
    `PackedVector2Array<class_PackedVector2Array>`)
-   `PackedVector2Array<class_PackedVector2Array>` **get\_polygon**()

A `Vector2<class_Vector2>` array with the index for polygon's vertices
positions.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector2Array<class_PackedVector2Array>` for more details.
