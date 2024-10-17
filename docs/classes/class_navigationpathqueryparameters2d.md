github\_url  
hide

# NavigationPathQueryParameters2D

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides parameters for 2D navigation path queries.

classref-introduction-group

## Description

By changing various properties of this object, such as the start and
target position, you can configure path queries to the
`NavigationServer2D<class_NavigationServer2D>`.

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

## Enumerations

classref-enumeration

enum **PathfindingAlgorithm**:
`🔗<enum_NavigationPathQueryParameters2D_PathfindingAlgorithm>`

classref-enumeration-constant

`PathfindingAlgorithm<enum_NavigationPathQueryParameters2D_PathfindingAlgorithm>`
**PATHFINDING\_ALGORITHM\_ASTAR** = `0`

The path query uses the default A\* pathfinding algorithm.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PathPostProcessing**:
`🔗<enum_NavigationPathQueryParameters2D_PathPostProcessing>`

classref-enumeration-constant

`PathPostProcessing<enum_NavigationPathQueryParameters2D_PathPostProcessing>`
**PATH\_POSTPROCESSING\_CORRIDORFUNNEL** = `0`

Applies a funnel algorithm to the raw path corridor found by the
pathfinding algorithm. This will result in the shortest path possible
inside the path corridor. This postprocessing very much depends on the
navigation mesh polygon layout and the created corridor. Especially
tile- or gridbased layouts can face artificial corners with diagonal
movement due to a jagged path corridor imposed by the cell shapes.

classref-enumeration-constant

`PathPostProcessing<enum_NavigationPathQueryParameters2D_PathPostProcessing>`
**PATH\_POSTPROCESSING\_EDGECENTERED** = `1`

Centers every path position in the middle of the traveled navigation
mesh polygon edge. This creates better paths for tile- or gridbased
layouts that restrict the movement to the cells center.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **PathMetadataFlags**:
`🔗<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`

classref-enumeration-constant

`PathMetadataFlags<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`
**PATH\_METADATA\_INCLUDE\_NONE** = `0`

Don't include any additional metadata about the returned path.

classref-enumeration-constant

`PathMetadataFlags<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`
**PATH\_METADATA\_INCLUDE\_TYPES** = `1`

Include the type of navigation primitive (region or link) that each
point of the path goes through.

classref-enumeration-constant

`PathMetadataFlags<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`
**PATH\_METADATA\_INCLUDE\_RIDS** = `2`

Include the `RID<class_RID>`s of the regions and links that each point
of the path goes through.

classref-enumeration-constant

`PathMetadataFlags<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`
**PATH\_METADATA\_INCLUDE\_OWNERS** = `4`

Include the `ObjectID`s of the `Object<class_Object>`s which manage the
regions and links each point of the path goes through.

classref-enumeration-constant

`PathMetadataFlags<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`
**PATH\_METADATA\_INCLUDE\_ALL** = `7`

Include all available metadata about the returned path.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`RID<class_RID>` **map** = `RID()`
`🔗<class_NavigationPathQueryParameters2D_property_map>`

classref-property-setget

-   `void (No return value.)` **set\_map**(value: `RID<class_RID>`)
-   `RID<class_RID>` **get\_map**()

The navigation map `RID<class_RID>` used in the path query.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`PathMetadataFlags<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`\]
**metadata\_flags** = `7`
`🔗<class_NavigationPathQueryParameters2D_property_metadata_flags>`

classref-property-setget

-   `void (No return value.)` **set\_metadata\_flags**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`PathMetadataFlags<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`PathMetadataFlags<enum_NavigationPathQueryParameters2D_PathMetadataFlags>`\]
    **get\_metadata\_flags**()

Additional information to include with the navigation path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **navigation\_layers** = `1`
`🔗<class_NavigationPathQueryParameters2D_property_navigation_layers>`

classref-property-setget

-   `void (No return value.)` **set\_navigation\_layers**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_navigation\_layers**()

The navigation layers the query will use (as a bitmask).

classref-item-separator

------------------------------------------------------------------------

classref-property

`PathPostProcessing<enum_NavigationPathQueryParameters2D_PathPostProcessing>`
**path\_postprocessing** = `0`
`🔗<class_NavigationPathQueryParameters2D_property_path_postprocessing>`

classref-property-setget

-   `void (No return value.)` **set\_path\_postprocessing**(value:
    `PathPostProcessing<enum_NavigationPathQueryParameters2D_PathPostProcessing>`)
-   `PathPostProcessing<enum_NavigationPathQueryParameters2D_PathPostProcessing>`
    **get\_path\_postprocessing**()

The path postprocessing applied to the raw path corridor found by the
`pathfinding_algorithm<class_NavigationPathQueryParameters2D_property_pathfinding_algorithm>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PathfindingAlgorithm<enum_NavigationPathQueryParameters2D_PathfindingAlgorithm>`
**pathfinding\_algorithm** = `0`
`🔗<class_NavigationPathQueryParameters2D_property_pathfinding_algorithm>`

classref-property-setget

-   `void (No return value.)` **set\_pathfinding\_algorithm**(value:
    `PathfindingAlgorithm<enum_NavigationPathQueryParameters2D_PathfindingAlgorithm>`)
-   `PathfindingAlgorithm<enum_NavigationPathQueryParameters2D_PathfindingAlgorithm>`
    **get\_pathfinding\_algorithm**()

The pathfinding algorithm used in the path query.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **simplify\_epsilon** = `0.0`
`🔗<class_NavigationPathQueryParameters2D_property_simplify_epsilon>`

classref-property-setget

-   `void (No return value.)` **set\_simplify\_epsilon**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_simplify\_epsilon**()

The path simplification amount in worlds units.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **simplify\_path** = `false`
`🔗<class_NavigationPathQueryParameters2D_property_simplify_path>`

classref-property-setget

-   `void (No return value.)` **set\_simplify\_path**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_simplify\_path**()

If `true` a simplified version of the path will be returned with less
critical path points removed. The simplification amount is controlled by
`simplify_epsilon<class_NavigationPathQueryParameters2D_property_simplify_epsilon>`.
The simplification uses a variant of Ramer-Douglas-Peucker algorithm for
curve point decimation.

Path simplification can be helpful to mitigate various path following
issues that can arise with certain agent types and script behaviors.
E.g. "steering" agents or avoidance in "open fields".

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **start\_position** = `Vector2(0, 0)`
`🔗<class_NavigationPathQueryParameters2D_property_start_position>`

classref-property-setget

-   `void (No return value.)` **set\_start\_position**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_start\_position**()

The pathfinding start position in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **target\_position** = `Vector2(0, 0)`
`🔗<class_NavigationPathQueryParameters2D_property_target_position>`

classref-property-setget

-   `void (No return value.)` **set\_target\_position**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_target\_position**()

The pathfinding target position in global coordinates.
