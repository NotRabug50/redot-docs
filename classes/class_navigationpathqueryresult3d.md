github\_url  
hide

# NavigationPathQueryResult3D

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Represents the result of a 3D pathfinding query.

classref-introduction-group

## Description

This class stores the result of a 3D navigation path query from the
`NavigationServer3D<class_NavigationServer3D>`.

classref-introduction-group

## Tutorials

-   `Using NavigationPathQueryObjects <../tutorials/navigation/navigation_using_navigationpathqueryobjects>`

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
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **PathSegmentType**:
`🔗<enum_NavigationPathQueryResult3D_PathSegmentType>`

classref-enumeration-constant

`PathSegmentType<enum_NavigationPathQueryResult3D_PathSegmentType>`
**PATH\_SEGMENT\_TYPE\_REGION** = `0`

This segment of the path goes through a region.

classref-enumeration-constant

`PathSegmentType<enum_NavigationPathQueryResult3D_PathSegmentType>`
**PATH\_SEGMENT\_TYPE\_LINK** = `1`

This segment of the path goes through a link.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PackedVector3Array<class_PackedVector3Array>` **path** =
`PackedVector3Array()`
`🔗<class_NavigationPathQueryResult3D_property_path>`

classref-property-setget

-   `void (No return value.)` **set\_path**(value:
    `PackedVector3Array<class_PackedVector3Array>`)
-   `PackedVector3Array<class_PackedVector3Array>` **get\_path**()

The resulting path array from the navigation query. All path array
positions are in global coordinates. Without customized query parameters
this is the same path as returned by
`NavigationServer3D.map_get_path<class_NavigationServer3D_method_map_get_path>`.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector3Array<class_PackedVector3Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedInt64Array<class_PackedInt64Array>` **path\_owner\_ids** =
`PackedInt64Array()`
`🔗<class_NavigationPathQueryResult3D_property_path_owner_ids>`

classref-property-setget

-   `void (No return value.)` **set\_path\_owner\_ids**(value:
    `PackedInt64Array<class_PackedInt64Array>`)
-   `PackedInt64Array<class_PackedInt64Array>`
    **get\_path\_owner\_ids**()

The `ObjectID`s of the `Object<class_Object>`s which manage the regions
and links each point of the path goes through.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedInt64Array<class_PackedInt64Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`RID<class_RID>`\] **path\_rids** = `[]`
`🔗<class_NavigationPathQueryResult3D_property_path_rids>`

classref-property-setget

-   `void (No return value.)` **set\_path\_rids**(value:
    `Array<class_Array>`\[`RID<class_RID>`\])
-   `Array<class_Array>`\[`RID<class_RID>`\] **get\_path\_rids**()

The `RID<class_RID>`s of the regions and links that each point of the
path goes through.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedInt32Array<class_PackedInt32Array>` **path\_types** =
`PackedInt32Array()`
`🔗<class_NavigationPathQueryResult3D_property_path_types>`

classref-property-setget

-   `void (No return value.)` **set\_path\_types**(value:
    `PackedInt32Array<class_PackedInt32Array>`)
-   `PackedInt32Array<class_PackedInt32Array>` **get\_path\_types**()

The type of navigation primitive (region or link) that each point of the
path goes through.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedInt32Array<class_PackedInt32Array>` for more details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **reset**()
`🔗<class_NavigationPathQueryResult3D_method_reset>`

Reset the result object to its initial state. This is useful to reuse
the object across multiple queries.
