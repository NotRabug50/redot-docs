github\_url  
hide

# StyleBoxLine

**Inherits:** `StyleBox<class_StyleBox>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A `StyleBox<class_StyleBox>` that displays a single line of a given
color and thickness.

classref-introduction-group

## Description

A `StyleBox<class_StyleBox>` that displays a single line of a given
color and thickness. The line can be either horizontal or vertical.
Useful for separators.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Color<class_Color>` **color** = `Color(0, 0, 0, 1)`
`🔗<class_StyleBoxLine_property_color>`

classref-property-setget

-   `void (No return value.)` **set\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_color**()

The line's color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **grow\_begin** = `1.0`
`🔗<class_StyleBoxLine_property_grow_begin>`

classref-property-setget

-   `void (No return value.)` **set\_grow\_begin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_grow\_begin**()

The number of pixels the line will extend before the **StyleBoxLine**'s
bounds. If set to a negative value, the line will begin inside the
**StyleBoxLine**'s bounds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **grow\_end** = `1.0`
`🔗<class_StyleBoxLine_property_grow_end>`

classref-property-setget

-   `void (No return value.)` **set\_grow\_end**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_grow\_end**()

The number of pixels the line will extend past the **StyleBoxLine**'s
bounds. If set to a negative value, the line will end inside the
**StyleBoxLine**'s bounds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **thickness** = `1`
`🔗<class_StyleBoxLine_property_thickness>`

classref-property-setget

-   `void (No return value.)` **set\_thickness**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_thickness**()

The line's thickness in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **vertical** = `false`
`🔗<class_StyleBoxLine_property_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_vertical**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_vertical**()

If `true`, the line will be vertical. If `false`, the line will be
horizontal.
