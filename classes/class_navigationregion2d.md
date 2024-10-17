github\_url  
hide

# NavigationRegion2D

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A traversable 2D region that
`NavigationAgent2D<class_NavigationAgent2D>`s can use for pathfinding.

classref-introduction-group

## Description

A traversable 2D region based on a
`NavigationPolygon<class_NavigationPolygon>` that
`NavigationAgent2D<class_NavigationAgent2D>`s can use for pathfinding.

Two regions can be connected to each other if they share a similar edge.
You can set the minimum distance between two vertices required to
connect two edges by using
`NavigationServer2D.map_set_edge_connection_margin<class_NavigationServer2D_method_map_set_edge_connection_margin>`.

\*\*Note:\*\* Overlapping two regions' navigation polygons is not enough
for connecting two regions. They must share a similar edge.

The pathfinding cost of entering a region from another region can be
controlled with the
`enter_cost<class_NavigationRegion2D_property_enter_cost>` value.

\*\*Note:\*\* This value is not added to the path cost when the start
position is already inside this region.

The pathfinding cost of traveling distances inside this region can be
controlled with the
`travel_cost<class_NavigationRegion2D_property_travel_cost>` multiplier.

\*\*Note:\*\* This node caches changes to its properties, so if you make
changes to the underlying region `RID<class_RID>` in
`NavigationServer2D<class_NavigationServer2D>`, they will not be
reflected in this node's properties.

classref-introduction-group

## Tutorials

-   `Using NavigationRegions <../tutorials/navigation/navigation_using_navigationregions>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**bake\_finished**() `🔗<class_NavigationRegion2D_signal_bake_finished>`

Emitted when a navigation polygon bake operation is completed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**navigation\_polygon\_changed**()
`🔗<class_NavigationRegion2D_signal_navigation_polygon_changed>`

Emitted when the used navigation polygon is replaced or changes to the
internals of the current navigation polygon are committed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **enabled** = `true`
`🔗<class_NavigationRegion2D_property_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_enabled**()

Determines if the **NavigationRegion2D** is enabled or disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **enter\_cost** = `0.0`
`🔗<class_NavigationRegion2D_property_enter_cost>`

classref-property-setget

-   `void (No return value.)` **set\_enter\_cost**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_enter\_cost**()

When pathfinding enters this region's navigation mesh from another
regions navigation mesh the
`enter_cost<class_NavigationRegion2D_property_enter_cost>` value is
added to the path distance for determining the shortest path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **navigation\_layers** = `1`
`🔗<class_NavigationRegion2D_property_navigation_layers>`

classref-property-setget

-   `void (No return value.)` **set\_navigation\_layers**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_navigation\_layers**()

A bitfield determining all navigation layers the region belongs to.
These navigation layers can be checked upon when requesting a path with
`NavigationServer2D.map_get_path<class_NavigationServer2D_method_map_get_path>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NavigationPolygon<class_NavigationPolygon>` **navigation\_polygon**
`🔗<class_NavigationRegion2D_property_navigation_polygon>`

classref-property-setget

-   `void (No return value.)` **set\_navigation\_polygon**(value:
    `NavigationPolygon<class_NavigationPolygon>`)
-   `NavigationPolygon<class_NavigationPolygon>`
    **get\_navigation\_polygon**()

The `NavigationPolygon<class_NavigationPolygon>` resource to use.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **travel\_cost** = `1.0`
`🔗<class_NavigationRegion2D_property_travel_cost>`

classref-property-setget

-   `void (No return value.)` **set\_travel\_cost**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_travel\_cost**()

When pathfinding moves inside this region's navigation mesh the traveled
distances are multiplied with
`travel_cost<class_NavigationRegion2D_property_travel_cost>` for
determining the shortest path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_edge\_connections** = `true`
`🔗<class_NavigationRegion2D_property_use_edge_connections>`

classref-property-setget

-   `void (No return value.)` **set\_use\_edge\_connections**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_edge\_connections**()

If enabled the navigation region will use edge connections to connect
with other navigation regions within proximity of the navigation map
edge connection margin.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **bake\_navigation\_polygon**(on\_thread:
`bool<class_bool>` = true)
`🔗<class_NavigationRegion2D_method_bake_navigation_polygon>`

Bakes the `NavigationPolygon<class_NavigationPolygon>`. If `on_thread`
is set to `true` (default), the baking is done on a separate thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_navigation\_layer\_value**(layer\_number:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationRegion2D_method_get_navigation_layer_value>`

Returns whether or not the specified layer of the
`navigation_layers<class_NavigationRegion2D_property_navigation_layers>`
bitmask is enabled, given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_navigation\_map**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationRegion2D_method_get_navigation_map>`

Returns the current navigation map `RID<class_RID>` used by this region.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_region\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationRegion2D_method_get_region_rid>`

**Deprecated:** Use `get_rid<class_NavigationRegion2D_method_get_rid>`
instead.

Returns the `RID<class_RID>` of this region on the
`NavigationServer2D<class_NavigationServer2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationRegion2D_method_get_rid>`

Returns the `RID<class_RID>` of this region on the
`NavigationServer2D<class_NavigationServer2D>`. Combined with
`NavigationServer2D.map_get_closest_point_owner<class_NavigationServer2D_method_map_get_closest_point_owner>`
can be used to identify the **NavigationRegion2D** closest to a point on
the merged navigation map.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_baking**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationRegion2D_method_is_baking>`

Returns `true` when the `NavigationPolygon<class_NavigationPolygon>` is
being baked on a background thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_navigation\_layer\_value**(layer\_number: `int<class_int>`,
value: `bool<class_bool>`)
`🔗<class_NavigationRegion2D_method_set_navigation_layer_value>`

Based on `value`, enables or disables the specified layer in the
`navigation_layers<class_NavigationRegion2D_property_navigation_layers>`
bitmask, given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_navigation\_map**(navigation\_map:
`RID<class_RID>`)
`🔗<class_NavigationRegion2D_method_set_navigation_map>`

Sets the `RID<class_RID>` of the navigation map this region should use.
By default the region will automatically join the
`World2D<class_World2D>` default navigation map so this function is only
required to override the default map.
